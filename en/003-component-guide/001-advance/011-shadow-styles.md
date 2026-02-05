---
id: shadow-styles
title: Shadow
description: Add shadow effect to the layer
parent: advance-component
previous: display-styles
next: transform-styles
order: 11
demos:
  - key: shadow-editor
    title: Shadow Example
    component: ShadowEditor
    sticky: true
    props:
      unique: true
---

# Shadow Style Component

_Adds shadow effects to layers, enhancing visual hierarchy and depth._

<!-- demo:shadow-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

The shadow list can add multiple shadow effects, each shadow effect can set the related properties.

## Horizontal Position

The horizontal offset of the shadow relative to the layer, supports numeric input, only supports the unit `px`.

## Vertical Position

The vertical offset of the shadow relative to the layer, supports numeric input, only supports the unit `px`.

## Blur Distance

Used to control the spread range of the shadow, supports numeric input, only supports positive numbers and the unit `px`.

## Shadow Size

Used to control the size of the shadow, supports numeric input, only supports positive numbers and the unit `px`.

## Shadow Color

The color of the shadow, supports color picker. Clicking the shadow color block will pop up the color picker, you can use the color palette, color picker or color code to select the color.

The color code mode allows switching, currently supports:

- RGB(A)
- HSL(A)
- HEX(A)

## Inner Shadow

After checking the `Inner Shadow` option, the shadow will be drawn inside the layer, rather than outside.