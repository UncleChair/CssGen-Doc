---
id: transform-styles
title: Transform
description: Transform the layer
parent: advance-component
previous: shadow-styles
next: custom-styles
order: 12
demos:
  - key: transform-editor
    title: Transform Example
    component: TransformEditor
    sticky: true
    props:
      unique: true
---

# Transform Style Component

_Perform transformation operations such as rotation, scaling, movement or tilt on the layer to create dynamic effects._

<!-- demo:transform-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

The transform list can add multiple transform effects, each transform effect can set the related properties.

## Anchor Setting

The anchor settings are used to determine the reference point of the layer transformation, such as the rotation center or scaling center, supports horizontal and vertical direction settings, supports numeric input, the unit is `%`.

## Horizontal Offset

Horizontal offset is used to control the offset distance of the layer in the horizontal direction, supports numeric input, the unit is `px`.

## Vertical Offset

Vertical offset is used to control the offset distance of the layer in the vertical direction, supports numeric input, the unit is `px`.

## Horizontal Scale

Horizontal scale is used to control the scale ratio of the layer in the horizontal direction, supports numeric input, the unit is `%`.

## Vertical Scale

Vertical scale is used to control the scale ratio of the layer in the vertical direction, supports numeric input, the unit is `%`.

## Vertical Rotate

Vertical rotate is used to control the rotation angle of the layer on the vertical (X) axis, supports numeric input, the unit is `deg`.

## Horizontal Rotate

Horizontal rotate is used to control the rotation angle of the layer on the horizontal (Y) axis, supports numeric input, the unit is `deg`.

## Rotate

Rotate is used to control the rotation angle of the layer on the plane (Z axis), supports numeric input, the unit is `deg`.
