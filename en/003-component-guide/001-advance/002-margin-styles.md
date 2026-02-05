---
id: margin-styles
title: Margin
description: Set the spacing between layers
parent: advance-component
previous: padding-styles
next: height-styles
order: 2
demos:
  - key: margin-editor
    title: Margin Example
    component: MarginEditor
    sticky: true
---

# Margin Style Component

_Margin is the area outside the border, usually used to control the spacing between layers._

<!-- demo:margin-editor -->

> The **Force Usage** option can be used to force override the style settings when the style adjustment is not functional on some platforms.

## Overall Adjustment

In overall mode, you can set the margin width in four directions at the same time, the number part can be input directly or dragged with the slider, supported negative numbers, in negative mode the adjacent layers will overlap, in positive mode the adjacent layers will be away from each other.
The supported units include:
- px<sup><a href="#ref1">[1]</a></sup>: Pixel, for ordinary screens, usually a device pixel
- pt<sup><a href="#ref2">[2]</a></sup>: Point
- em<sup><a href="#ref3">[3]</a></sup>: Element font size
- vh<sup><a href="#ref4">[4]</a></sup>: Percentage of viewport height
- vw<sup><a href="#ref5">[5]</a></sup>: Percentage of viewport width

The default unit is px, you can also manually input other units<sup><a href="#ref6">[6]</a></sup>.

## Single Side Adjustment

In detailed adjustment mode, you can set the margin width in four directions separately, the supported numbers and units are the same as in overall adjustment mode.

## **Reference**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#px)
<span id="ref2">[2]</span> [MDN length unit pt](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref3">[3]</span> [MDN length unit em](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#em)
<span id="ref4">[4]</span> [MDN length unit vh](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref5">[5]</span> [MDN length unit vw](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref6">[6]</span> [MDN length](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/length)