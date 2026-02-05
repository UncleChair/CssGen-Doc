---
id: display-styles
title: Display
description: Control the display and layout of the layer
parent: advance-component
previous: position-styles
next: shadow-styles
order: 10
demos:
  - key: display-editor-simple
    title: Display Example
    component: DisplayEditorSimple
    sticky: true
    props:
      unique: true
---

# Display Style Component

_Control the display and layout of the layer on the page._

<!-- demo:display-editor-simple -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

## Display Mode Options<sup><a href="#ref1">[1]</a></sup>

### Hidden (none)

The layer will be hidden and will not be displayed on the page or occupy any space.

### Default (unset)

The layer will be displayed in the default way, in most cases equivalent to the `block` display mode.

### Flex (flex)

Enable the powerful flex layout mode, which can flexibly control the horizontal and vertical layout.

#### Main Axis Direction

The main direction of the layout, similar to the direction of the team arrangement, the default is horizontal arrangement.

**Options**: 
- **Left to Right (row)**
- **Right to Left (row-reverse)**
- **Up to Down (column)**
- **Down to Up (column-reverse)**

#### Main Axis Alignment<sup><a href="#ref2">[2]</a></sup>

Control the distribution of the layout on the main axis direction.

**Options**: 
- **Start (flex-start)**: All layers are aligned at the starting end
- **End (flex-end)**: All layers are aligned at the end
- **Center (center)**: All layers are centered
- **Between (space-between)**: The layers are evenly distributed, the first and last layers are aligned at the edges
- **Around (space-around)**: The layers are evenly distributed, each layer is allocated the same space around it
- **Evenly (space-evenly)**: The layers are evenly distributed, the interval between each layer is equal

#### Cross Axis<sup><a href="#ref3">[3]</a></sup>

The cross axis is perpendicular to the main axis, if the main axis is horizontal, the cross axis is vertical; if the main axis is vertical, the cross axis is horizontal.

**Options**: 
- **Stretch (stretch)**: The layers are stretched to fill the container
- **Center (center)**: The layers are centered
- **Start (start)**: The layers are aligned at the starting end
- **End (end)**: The layers are aligned at the end

### Block (block)

Control whether to wrap when a line/column cannot fit all layers.

### Inline (inline)

Make the layers appear like text, multiple layers will be lined up next to each other in the same row.

## Overflow Settings<sup><a href="#ref4">[4]</a></sup>

When the layer content exceeds the layer size, control whether to display the overflow part.

**Visible (visible)**: 
- The content will overflow and not be clipped

**Hidden (hidden)**: 
- The overflow part will be clipped and not displayed

## **Reference**

<span id="ref1">[1]</span> [CSS - display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
<span id="ref2">[2]</span> [CSS - justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)
<span id="ref3">[3]</span> [CSS - align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)
<span id="ref4">[4]</span> [CSS - overflow](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)