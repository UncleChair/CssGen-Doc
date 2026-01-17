---
id: width-styles
title: 宽度样式
description: 定制宽度样式
parent: advance-component
previous: height-styles
order: 4
demos:
  - key: width-editor
    title: 宽度示例
    component: WidthEditor
    sticky: true
---

# 宽度样式组件

_宽度指的是图层显示内容区域的宽度。_

<!-- demo:width-editor -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

___绝大部分情况下您都不需要使用宽度组件，因为大部分的内容都应当自适应调整它们的大小。___

## 数值调整

数值调整可以设置图层显示内容区域的宽度，数字部分可以通过直接输入或拖动滑块输入，只支持正数，支持的单位包括:
- px<sup><a href="#ref1">[1]</a></sup>: 像素，对于普通的屏幕，通常是一个设备像素（点）
- pt<sup><a href="#ref2">[2]</a></sup>: 磅（point）
- em<sup><a href="#ref3">[3]</a></sup>: 元素字体大小值
- vh<sup><a href="#ref4">[4]</a></sup>: 相对于视口高度的百分比
- vw<sup><a href="#ref5">[5]</a></sup>: 相对于视口宽度的百分比

默认单位为 px，您也可以手动输入其他单位<sup><a href="#ref6">[6]</a></sup>。

如果您希望图层宽度自适应内容大小，可以勾选 `启用自适应` 选项。

## 大小限制

在某些情况下，您可能希望限制图层宽度的大小，可以勾选 `最大限制` 或 `最小限制` 选项，并设置最大或最小宽度，单位与数值调整部分一致。

## 百分比调整

当您的图层定位修改为 `独立` 时，您可以设置图层宽度相对于其 `定位基点` 的百分比，此时的宽度将会根据 `定位基点` 的百分比大小和您设置的数值进行计算，数值输入在这种模式下支持负数。

## **参考资料**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#px)
<span id="ref2">[2]</span> [MDN length unit pt](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref3">[3]</span> [MDN length unit em](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#em)
<span id="ref4">[4]</span> [MDN length unit vh](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref5">[5]</span> [MDN length unit vw](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref6">[6]</span> [MDN length](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length)