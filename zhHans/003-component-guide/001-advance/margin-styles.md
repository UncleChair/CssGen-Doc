---
id: margin-styles
title: 外边距样式
description: 定制外边距样式
parent: advance-component
previous: padding-styles
next: height-styles
order: 2
demos:
  - key: margin-editor
    title: 外边距示例
    component: MarginEditor
    sticky: true
---

# 外边距样式组件

_外边距区域位于边框外，通常用以控制图层之间的间距。_

<!-- demo:margin-editor -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

## 整体调整

在整体调整模式下，您可以同时设置四个方向的外边距宽度，数字部分可以通过直接输入或拖动滑块输入，支持负数，负数模式下临近图层将会重叠，正数模式下将会远离临近图层。
单位部分支持包括:
- px<sup><a href="#ref1">[1]</a></sup>: 像素，对于普通的屏幕，通常是一个设备像素（点）
- pt<sup><a href="#ref2">[2]</a></sup>: 磅（point）
- em<sup><a href="#ref3">[3]</a></sup>: 元素字体大小值
- vh<sup><a href="#ref4">[4]</a></sup>: 相对于视口高度的百分比
- vw<sup><a href="#ref5">[5]</a></sup>: 相对于视口宽度的百分比

默认单位为 px，您也可以手动输入其他单位<sup><a href="#ref6">[6]</a></sup>。

## 单边调整

在单边调整模式下，您可以单独设置四个方向的外边距宽度，支持的数字和单位与整体调整模式相同。

## **参考资料**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#px)
<span id="ref2">[2]</span> [MDN length unit pt](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref3">[3]</span> [MDN length unit em](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#em)
<span id="ref4">[4]</span> [MDN length unit vh](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref5">[5]</span> [MDN length unit vw](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref6">[6]</span> [MDN length](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length)