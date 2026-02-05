---
id: position-styles
title: Position
description: Control the position of the layer in the page
parent: advance-component
previous: background-styles
next: display-styles
order: 9
demos:
  - key: position-editor
    title: Position Example
    component: PositionEditor
    sticky: true
    props:
      unique: true
---

# Position Style Component

_Control the position of the layer in the page._

<!-- demo:position-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

## What is Position

In web design, **position**<sup><a href="#ref1">[1]</a></sup> determines the position and display mode of the layer on the page. Just like placing photos on paper, you can choose to: 
- Place in order (default way)
- Move a little distance relative to the original position
- Fix at a certain position on the paper

Through the positioning function, you can precisely control the position of each layer, and achieve various complex page layout effects.

## Position Mode

The position component provides multiple positioning modes, each with its specific purpose: 

### None (Default)

This is the default state of most layers. The layer will be arranged according to the normal document flow of the page, just like adding content in the document in order, most layers default to no positioning.

**Applicable Scenarios**: 
- Ordinary text paragraphs
- Ordered lists
- Content that does not require special position control

### Relative Position

The layer is offset from its original position. After using relative positioning, you can move it up, down, left, and right by a certain distance, but the space it originally occupies is still reserved.

**Features**: 
- The layer moves, the original position is still occupied
- The original position is still occupied after the layer moves
- Can be used as the positioning base point for sub-layers

**Applicable Scenarios**: 
- The position needs to be adjusted but does not affect the layout
- Used as the datum point for sub-layers of absolute positioning

### Absolute Position

The layer leaves the normal document flow and is positioned relative to the nearest "datum" (a positioned parent layer). If there is no such parent layer, it is positioned relative to the entire page.

**Characteristics**: 
- Completely leaves the document flow and does not take up space
- Other layers ignore its presence

**Applicable Scenarios**: 
- Decorative elements that require precise positioning
- Overlay or mask layers

## Position Offset

When the layer uses the positioning mode (except for "no positioning"), you can set the `anchor` and `offset value` to precisely control the position of the layer: 

- **Horizontal Anchor**: Adjust the horizontal alignment anchor of the layer, the optional values are `Left` , `Center` , `Right`
- **Horizontal Offset**: Adjust the position of the layer in the horizontal direction, the unit is `px`
- **Vertical Anchor**: Adjust the vertical alignment anchor of the layer, the optional values are `Top` , `Center` , `Bottom`
- **Vertical Offset**: Adjust the position of the layer in the vertical direction, the unit is `px`

## Datum Point

**Datum Point** is an important concept: When the positioning mode of the layer is not "no positioning", it becomes the reference point for its sub-layers.

**Working Principle**: 
1. When the sub-layer uses absolute positioning, it is positioned relative to the nearest "datum" (a positioned parent layer).
2. If the parent layer is "no positioning", the sub-layer will continue to search upwards until a datum point is found.
3. If it cannot be found, it is positioned relative to the entire page.

**Practice Techniques**: 
- Common practice: Set "datum" for the parent container and "absolute positioning" for the sub-element.
- This way the sub-element will be positioned relative to the parent container, rather than the entire page.
- If the "relative positioning" of the parent container is not set with any offset value, it looks like "no positioning", but can be used as a datum point.

## Layer Adjustment

When the layer uses the positioning mode (except for "no positioning"), you can set the `layer` to adjust the layer level, in most cases the higher the level, the closer the layer is to the front, but it should be noted that only layers with the same datum point will affect each other's level<sup><a href="#ref2">[2]</a></sup>.

> Position is a very complex concept in CSS, in many cases you need to familiarize yourself with the positioning properties of CSS to better use the positioning component.

## **Reference**

<span id="ref1">[1]</span> [MDN - position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)  
<span id="ref3">[2]</span> [MDN - level adjustment](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)