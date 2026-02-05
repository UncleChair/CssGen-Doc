---
id: height-styles
title: Height
description: Set the height of the layer content area
parent: advance-component
previous: margin-styles
next: width-styles
order: 3
demos:
  - key: height-editor
    title: Height Example
    component: HeightEditor
    sticky: true
---

# Height Style Component

_Height refers to the height of the layer content area, used to control the vertical size of the layer content area._

<!-- demo:height-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

___Most of the time you don't need to use the height component, because most of the content should be adjusted to fit the size of the content responsively._

## Number Adjustment

Number adjustment can set the height of the layer content area, the number part can be input directly or dragged with the slider, only positive numbers are supported, the supported units include:
- px<sup><a href="#ref1">[1]</a></sup>: Pixel, for ordinary screens, usually a device pixel
- pt<sup><a href="#ref2">[2]</a></sup>: Point
- em<sup><a href="#ref3">[3]</a></sup>: Element font size
- vh<sup><a href="#ref4">[4]</a></sup>: Percentage of viewport height
- vw<sup><a href="#ref5">[5]</a></sup>: Percentage of viewport width

The default unit is px, you can also manually input other units<sup><a href="#ref6">[6]</a></sup>.

If you want the layer height to adapt to the content size, you can check the `Enable Adaptation` option.

## Size Limit

In some cases, you may want to limit the size of the layer height, you can check the `Max Limit` or `Min Limit` option, and then set the maximum or minimum value, the units are the same as the number adjustment part.

## Percentage Adjustment

When your layer positioning is modified to `Absolute`, you can set the percentage of the layer height relative to its `Datum`, the height will be calculated based on the percentage of the `Datum` and the value you set, the value input in this mode supports negative numbers.

## **Reference**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#px)
<span id="ref2">[2]</span> [MDN length unit pt](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref3">[3]</span> [MDN length unit em](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#em)
<span id="ref4">[4]</span> [MDN length unit vh](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref5">[5]</span> [MDN length unit vw](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref6">[6]</span> [MDN length](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length)