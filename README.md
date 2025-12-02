# CSSGen 文档系统开发指南

<p align="center">
  <a href="./README_en.md"><img alt="README in English" src="https://img.shields.io/badge/English-DFE0E5"></a>
  <a href="./README.md"><img alt="简体中文版自述文件" src="https://img.shields.io/badge/简体中文-DBEDFA"></a>
</p>

_文档系统为 CSSGen 项目的子项目，不支持独立部署_

本文档主要说明如何编写文档文件和添加组件。

## 📚 目录

- [文档系统概述](#文档系统概述)
- [编写文档文件](#编写文档文件)
  - [文件位置和命名](#文件位置和命名)
  - [Front Matter 元数据](#front-matter-元数据)
  - [Markdown 内容编写](#markdown-内容编写)
  - [添加组件演示](#添加组件演示)
- [添加组件](#添加组件)
  - [注册组件（开发人员）](#注册组件（开发人员）)
  - [在文档中使用组件](#在文档中使用组件)
- [多语言支持](#多语言支持)
- [最佳实践](#最佳实践)

---

## 文档系统概述

CSSGen 使用基于 Markdown 的文档系统，支持：

- ✅ 自动扫描和加载文档
- ✅ 多语言支持（中文、英文、日文）
- ✅ 交互式组件演示
- ✅ 自动生成文档导航树
- ✅ Front Matter 元数据管理
- ✅ 文档翻页导航（上一页/下一页）

文档系统会自动扫描 `public/docs/{locale}/` 目录下的所有 `.md` 文件，并根据 Front Matter 中的元数据自动生成文档列表和导航。

---

## 编写文档文件

### 文件位置和命名

文档文件应放置在以下目录结构中：

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

**命名规范：**
- 使用小写字母和连字符（kebab-case），例如：`text-styles.md`
- 文件名应该简洁且具有描述性
- 避免使用空格和特殊字符

### Front Matter 元数据

每个文档文件必须在开头包含 Front Matter（YAML 格式的元数据）：

```yaml
---
id: text-styles              # 必需：文档唯一标识符
title: 文本样式              # 必需：文档标题
description: 文本样式组件提供了全面的文字外观控制能力  # 可选：文档描述
order: 10                    # 可选：排序顺序（数字越小越靠前，默认为 999）
parent: style-guide          # 可选：父文档 ID（用于构建文档树）
previous: introduction       # 可选：上一页文档 ID（用于翻页导航）
next: border-styles          # 可选：下一页文档 ID（用于翻页导航）
demos:                       # 可选：组件演示配置
  - key: text-color
    title: 文本颜色示例
    component: TextColor
    props:
      selector: .demo-text-color
---
```

#### Front Matter 字段说明

| 字段 | 类型 | 必需 | 说明 |
|------|------|------|------|
| `id` | string | ✅ | 文档的唯一标识符，用于路由和引用 |
| `title` | string | ✅ | 文档标题，显示在导航和页面中 |
| `description` | string | ❌ | 文档描述，显示在翻页按钮中 |
| `order` | number | ❌ | 排序顺序，数字越小越靠前（默认 0） |
| `parent` | string | ❌ | 父文档的 ID，用于构建文档树结构 |
| `previous` | string | ❌ | 上一页文档的 ID，用于翻页导航 |
| `next` | string | ❌ | 下一页文档的 ID，用于翻页导航 |
| `demos` | array | ❌ | 组件演示配置数组（见下方说明） |

#### Demos 配置

`demos` 数组用于配置文档中使用的组件演示：

```yaml
demos:
  - key: demo-key              # 必需：演示的唯一标识符，用于后续插入组件
    title: 演示标题            # 可选：演示标题
    component: ComponentName   # 必需：组件注册名称，需与后续的注册字段一致
    props:                     # 可选：传递给组件的 props
      selector: .demo-element
      otherProp: value
```

**示例：**

```yaml
---
id: text-styles
title: 文本样式
demos:
  - key: text-color
    title: 文本颜色示例
    component: TextColor
    props:
      selector: .demo-text-color
  - key: text-shadow
    title: 文本阴影示例
    component: TextShadow
    props:
      selector: .demo-text-shadow
---
```

### Markdown 内容编写

Front Matter 之后是标准的 Markdown 内容：

```markdown
# 文本样式组件

文本样式组件提供了全面的文字外观控制能力。

## TextColor - 文本颜色

`TextColor` 组件用于设置文本的颜色。

### 功能特性

- 🎨 颜色选择器界面
- 支持 RGB、HEX、RGBA 格式
- 实时颜色预览
- 透明度控制
```

**支持的 Markdown 特性：**
- 标准 Markdown 语法
- GitHub Flavored Markdown (GFM)
- 表格

### 添加组件演示

在 Markdown 内容中，使用 HTML 注释来标记组件演示的插入位置：

```markdown
## 文本颜色示例

这里是一些说明文字...

<!-- demo:text-color -->

继续其他内容...
```

**说明：**
- `<!-- demo:demoKey -->` 中的 `demoKey` 必须与 Front Matter 中 `demos` 数组里的 `key` 匹配
- 组件会在该位置自动渲染
- 可以多次使用同一个 demo，只需在多个位置插入相同的注释，不过需要注意一般情况下相同的demo共享所有CSS状态变化

**完整示例：**

```markdown
---
id: text-styles
title: 文本样式
demos:
  - key: text-color
    title: 文本颜色示例
    component: TextColor
    props:
      selector: .demo-text-color
---

# 文本样式组件

## TextColor 组件

`TextColor` 组件用于设置文本的颜色。

### 功能特性

- 颜色选择器界面
- 支持多种颜色格式
- 实时预览

### 交互式演示

下面是一个可交互的演示：

<!-- demo:text-color -->

你可以通过上面的控件实时调整文本颜色。
```

---

## 添加组件

### 注册组件（开发人员）

#### 1. 导入组件

在 `components.registry.js` 中导入组件：

```javascript
import TextColor from '@/path';
// 导入其他组件...
```

#### 2. 注册组件

在 `initializeComponentRegistry` 函数中注册组件：

```javascript
export function initializeComponentRegistry() {
    ...
    // 使用 markRaw 避免组件被响应式化，提升性能
    registry.register('TextColor', markRaw(TextColor));
    registry.register('TextShadow', markRaw(TextShadow));
    ...
}
```

**重要提示：**

- 使用 `markRaw()` 包装组件，避免 Vue 的响应式系统处理组件对象，提升性能
- 注册名称（如 `'TextColor'`）必须与文档 Front Matter 中的 `component` 字段匹配

### 在文档中使用组件

#### 1. 在 Front Matter 中配置

```yaml
---
id: my-document
title: 我的文档
demos:
  - key: my-demo
    title: 我的演示
    component: TextColor  # 必须与注册名称匹配
    props:
      selector: .demo-element
      # 其他 props...
---
```

#### 2. 在 Markdown 中插入

```markdown
## 演示部分

这里是一些说明文字...

<!-- demo:my-demo -->

继续其他内容...
```

---

## 多语言支持

### 语言目录结构

文档系统支持多语言，每种语言的文档放在对应的目录下：

```
public/docs/
├── en/          # 英文文档
├── zhHans/      # 简体中文文档
├── ja/          # 日文文档
└── ...

```

### 语言配置（开发人员）

支持的语言字段需要在 `locale.config.js` 中配置：

```javascript
export const supportedLocales = ['en', 'zhHans', 'ja'];
```

### 创建多语言文档

1. 为每种语言创建对应的目录（如果不存在）
2. 在对应目录下创建相同结构的文档文件
3. 使用相同的 `id`，但可以有不同的 `title` 和内容

**示例：**

```
public/docs/
├── en/
│   └── introduction.md    # id: introduction, title: Introduction
└── zhHans/
    └── introduction.md    # id: introduction, title: 介绍
```

---

## 最佳实践

### 文档编写

1. **保持一致性**
   - 使用统一的文档结构和格式
   - 保持标题层级清晰（建议最多 4 级）
   - 使用一致的代码示例风格

2. **内容组织**
   - 每个文档应该专注于一个主题
   - 使用 `parent` 字段构建文档树结构
   - 合理使用 `order` 字段控制文档顺序
   - 使用 `previous` 和 `next` 字段创建文档阅读顺序，翻页按钮会自动显示在文档底部

3. **组件演示**
   - 为每个重要的功能提供交互式演示
   - 在演示前后提供清晰的说明文字
   - 确保演示的 `key` 具有描述性


---

## 常见问题

### Q: 文档没有显示在导航中？

**A:** 检查以下几点：

1. 确认文档文件在正确的语言目录下
2. 确认 Front Matter 中包含必需的 `id` 和 `title` 字段
3. 检查浏览器控制台是否有错误信息

### Q: 组件演示没有显示？

**A:** 检查以下几点：
1. 确认组件已在 `components.registry.js` 中注册
2. 确认 Front Matter 中的 `component` 名称与注册名称完全匹配
3. 确认 Markdown 中的 `<!-- demo:key -->` 与 Front Matter 中的 `key` 匹配
4. 检查组件 props 是否正确传递

### Q: 如何调整文档顺序？

**A:** 在 Front Matter 中使用 `order` 字段，数字越小越靠前：

```yaml
---
id: intro
title: 介绍
order: 0    # 最靠前
---
```

### Q: 如何创建文档树结构？

**A:** 使用 `parent` 字段指定父文档：

```yaml
---
id: text-styles
title: 文本样式
parent: style-guide  # 父文档的 id
---
```

### Q: 如何添加翻页导航？

**A:** 在 Front Matter 中使用 `previous` 和 `next` 字段指定相邻文档：

```yaml
---
id: style-guide
title: 样式指南
previous: introduction  # 上一页文档的 id
next: border-styles     # 下一页文档的 id
---
```

**说明：**
- 如果文档存在 `previous` 或 `next` 字段，翻页按钮会自动显示在文档底部
- 翻页按钮会显示相邻文档的标题和描述（如果有）
- 可以只设置 `previous` 或只设置 `next`，也可以两者都设置
- 如果相邻文档不存在或未找到，对应的翻页按钮不会显示

---

如有问题或建议，请提交 Issue 或 Pull Request。
