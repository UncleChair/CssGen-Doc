---
id: pseudo-element
title: Pre/Post Attached Layer
description: Add extra decorative layer
parent: advance-component
previous: custom-styles
order: 14
demos:
  - key: pseudo-element
    title: Attached Layer Example
    component: PseudoElement
    sticky: true
    props:
      unique: true
---

# Pre/Post Attached Layer

_Add extra decorative layers in front or behind the layer to achieve special decorative effects._

<!-- demo:pseudo-element -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

Pre/Post Attached Layer is essentially an extra added layer, except for some default properties and basic layers, you can adjust them like ordinary layers.

Note that attached layers are embedded inside the layer by default. You can first add the **Position** component to adjust the position of the attached layer, then set **Width** and **Height** to adjust its size (provided that **Display** is set to something other than **Inline** first).

The attached layer has an extra property **Content Text**, where you can enter any text you want to display.