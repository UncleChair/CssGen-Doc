# CSSGen Documentation System Development Guide

<p align="center">
  <a href="./README_en.md"><img alt="README in English" src="https://img.shields.io/badge/English-DBEDFA"></a>
  <a href="./README.md"><img alt="简体中文版自述文件" src="https://img.shields.io/badge/简体中文-DFE0E5"></a>
</p>

_Documentation System is a subproject of CSSGen project, it does not support standalone deployment_

This document explains how to write documentation files and add components.

## 📚 Table of Contents

- [Documentation System Overview](#documentation-system-overview)
- [Writing Documentation Files](#writing-documentation-files)
  - [File Location and Naming](#file-location-and-naming)
  - [Front Matter Metadata](#front-matter-metadata)
  - [Markdown Content Writing](#markdown-content-writing)
  - [Adding Component Demos](#adding-component-demos)
- [Adding Components](#adding-components)
  - [Registering Components (Developers)](#registering-components-developers)
  - [Using Components in Documentation](#using-components-in-documentation)
- [Multi-language Support](#multi-language-support)
- [Best Practices](#best-practices)

---

## Documentation System Overview

CSSGen uses a Markdown-based documentation system, supporting:

- ✅ Automatically scan and load documents
- ✅ Multi-language support (Chinese, English, Japanese)
- ✅ Interactive component demos
- ✅ Automatic generation of document navigation trees
- ✅ Front Matter metadata management
- ✅ Document pagination navigation (previous/next)

The documentation system automatically scans all `.md` files in the `public/docs/{locale}/` directory and automatically generates document lists and navigation based on the metadata in Front Matter.

---

## Writing Documentation Files

### File Location and Naming

Documentation files should be placed in the following directory structure:

```
public/docs/
├── en/              # 英文文档
│   ├── introduction.md
│   └── ...
├── zhHans/          # 简体中文文档
│   ├── introduction.md
│   ├── text-styles.md
│   └── ...
└── README.md        # 本文档
```

**Naming Conventions:**
- Use lowercase letters and hyphens (kebab-case), for example: `text-styles.md`
- The file name should be concise and descriptive
- Avoid using spaces and special characters

### Front Matter Metadata

Each documentation file must start with Front Matter (metadata in YAML format):

```yaml
---
id: text-styles              # Required: Document unique identifier
title: Text Styles              # Required: Document title
description: Text Styles component provides comprehensive text appearance control capabilities  # Optional: Document description
order: 10                    # Optional: Sort order (the smaller the number, the earlier it appears, default is 999)
parent: style-guide          # Optional: Parent document ID (for building document tree)
previous: introduction       # Optional: Previous document ID (for pagination navigation)
next: border-styles          # Optional: Next document ID (for pagination navigation)
demos:                       # Optional: Component demo configuration
  - key: text-color
    title: Text Color Example
    component: TextColor
    props:
      selector: .demo-text-color
---
```

#### Front Matter Fields Description

| Field | Type | Required | Description |
|------|------|------|------|
| `id` | string | ✅ | Document unique identifier, used for routing and reference |
| `title` | string | ✅ | Document title, displayed in navigation and page |
| `description` | string | ❌ | Document description, displayed in pagination buttons |
| `order` | number | ❌ | Sort order, the smaller the number, the earlier it appears (default is 0) |
| `parent` | string | ❌ | Parent document ID, used for building document tree structure |
| `previous` | string | ❌ | Previous document ID, used for pagination navigation |
| `next` | string | ❌ | Next document ID, used for pagination navigation |
| `demos` | array | ❌ | Component demo configuration array (see below for details) |

#### Demos Configuration

`demos` array is used to configure component demos used in the documentation:

```yaml
demos:
  - key: demo-key              # Required: Demo unique identifier, used for subsequent component insertion
    title: Demo Title          # Optional: Demo title
    component: ComponentName   # Required: Component registration name, must match the subsequent registration field
    props:                     # Optional: props passed to the component
      selector: .demo-element
      otherProp: value
```

**Example:**

```yaml
---
id: text-styles
title: Text Styles
demos:
  - key: text-color
    title: Text Color Example
    component: TextColor
    props:
      selector: .demo-text-color
  - key: text-shadow
    title: Text Shadow Example
    component: TextShadow
    props:
      selector: .demo-text-shadow
---
```

### Markdown Content Writing

After Front Matter, it is standard Markdown content:

```markdown
# Text Styles Component

Text Styles component provides comprehensive text appearance control capabilities.

## TextColor - Text Color

`TextColor` component is used to set the color of text.

### Features

- 🎨 Color selector interface
- Supports RGB, HEX, RGBA formats
- Real-time color preview
- Transparency control
```

**Supported Markdown Features:**
- Standard Markdown syntax
- GitHub Flavored Markdown (GFM)
- Tables

### Adding Component Demos

In Markdown content, use HTML comments to mark the insertion location of component demos:

```markdown
## Text Color Example

There are some explanatory text...

<!-- demo:text-color -->

Continue other content...
```

**Notes:**
- `demoKey` in `<!-- demo:demoKey -->` must match the `key` in the `demos` array in Front Matter
- The component will be rendered at this location automatically
- You can use the same demo multiple times, just insert the same comment in multiple locations, but note that in most cases the same demo shares all CSS state changes

**Complete Example:**

```markdown
---
id: text-styles
title: Text Styles
demos:
  - key: text-color
    title: Text Color Example
    component: TextColor
    props:
      selector: .demo-text-color
---

# Text Styles Component

## TextColor Component

`TextColor` component is used to set the color of text.

### Features

- Color selector interface
- Supports multiple color formats
- Real-time preview

### Interactive Demo

Here is an interactive demo:

<!-- demo:text-color -->

You can adjust the text color in real time through the controls above.
```

---

## Adding Components

### Registering Components (Developers)

#### 1. Import Components

In `components.registry.js` import components:

```javascript
import TextColor from '@/path';
// Import other components...
```

#### 2. Register Components

In `initializeComponentRegistry` function register components:

```javascript
export function initializeComponentRegistry() {
    ...
    registry.register('TextColor', markRaw(TextColor));
    registry.register('TextShadow', markRaw(TextShadow));
    ...
}
```

**Important Notes:**

- Use `markRaw()` to wrap components, avoid Vue's reactive system processing component objects, improve performance
- Registration name (e.g. `'TextColor'`) must match the `component` field in the document Front Matter

### Using Components in Documentation

#### 1. Configure in Front Matter

```yaml
---
id: my-document
title: My Document
demos:
  - key: my-demo
    title: My Demo
    component: TextColor  # Must match the registration name
    props:
      selector: .demo-element
      # Other props...
---
```

#### 2. Insert in Markdown

```markdown
## Demo Section

There are some explanatory text...

<!-- demo:my-demo -->

Continue other content...
```

---

## Multi-language Support

### Language Directory Structure

The documentation system supports multiple languages, and the documents for each language are placed in the corresponding directory:

```
public/docs/
├── en/          # English documents
├── zhHans/      # Simplified Chinese documents
├── ja/          # Japanese documents
└── ...

```

### Creating Multi-language Documents

1. Create a corresponding directory for each language (if it does not exist)
2. Create document files with the same structure in the corresponding directory
3. Use the same `id`, but can have different `title` and content

**Example:**

```
public/docs/
├── en/
│   └── introduction.md    # id: introduction, title: Introduction
└── zhHans/
    └── introduction.md    # id: introduction, title: 介绍
```

---

## Best Practices

### Writing Documentation

1. **Consistency**
   - Use consistent document structure and format
   - Keep the title hierarchy clear (recommended up to 4 levels)
   - Use consistent code example style

2. **Content Organization**
   - Each document should focus on a single topic
   - Use `parent` field to build document tree structure
   - Use `order` field to control document order
   - Use `previous` and `next` fields to create document reading order, the pagination buttons will be automatically displayed at the bottom of the document

3. **Component Demos**
   - Provide interactive demos for each important feature
   - Provide clear explanatory text before and after the demo
   - Ensure the `key` of the demo has a descriptive name

---

## Common Issues

### Q: Document not displayed in navigation?

**A:** Check the following几点：

1. Confirm that the document file is in the correct language directory
2. Confirm that the `id` and `title` fields are required in Front Matter
3. Check the browser console for error messages

### Q: Component demo not displayed?

**A:** Check the following:
1. Confirm that the component is registered in `components.registry.js`
2. Confirm that the `component` name in Front Matter matches the registration name
3. Confirm that the `<!-- demo:key -->` in Markdown matches the `key` in Front Matter
4. Check that the component props are correctly passed

### Q: How to adjust document order?

**A:** Use the `order` field in Front Matter, the smaller the number, the earlier it appears:

```yaml
---
id: intro
title: Introduction
order: 0    # The first one
---
```

### Q: How to create document tree structure?

**A:** Use the `parent` field to specify the parent document:

```yaml
---
id: text-styles
title: Text Styles
parent: style-guide  # The parent document id
---
```

### Q: How to add pagination navigation?

**A:** Use the `previous` and `next` fields in Front Matter to specify the adjacent documents:

```yaml
---
id: style-guide
title: Style Guide
previous: introduction  # The previous document id
next: border-styles     # The next document id
---
```

**Notes:**
- If the document has `previous` or `next` fields, the pagination buttons will be automatically displayed at the bottom of the document
- The pagination buttons will display the title and description of the adjacent document (if any)
- Can only set `previous` or `next`, or both
- If the adjacent document does not exist or is not found, the corresponding pagination button will not be displayed

---

If you have any questions or suggestions, please submit an Issue or Pull Request.
