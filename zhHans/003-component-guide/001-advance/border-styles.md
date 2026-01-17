---
id: border-styles
title: 边框样式
description: 定制边框样式
parent: advance-component
previous: advance-component
next: padding-styles
order: 0
demos:
  - key: border-editor
    title: 边框示例
    component: BorderEditor
    sticky: true
---

# 边框样式组件

_边框为图层周围的边框区域，包含基础线条边框和图片边框两种类型。_

<!-- demo:border-editor -->


> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

## 普通模式

在普通模式下,您可以设置基础的线条边框,包括边框样式<sup><a href="#ref1">[1]</a></sup>、边框宽度<sup><a href="#ref2">[2]</a></sup>和边框颜色<sup><a href="#ref3">[3]</a></sup>。

### 边框样式

边框样式包含:

- 实线: <div style="border-top:solid 4px; width: 100px;"></div>

- 虚线: <div style="border-top:dashed 4px; width: 100px;"></div>

- 点线: <div style="border-top:dotted 4px; width: 100px;"></div>

- 双实线: <div style="border-top:double 4px; width: 100px;"></div>

> 在未设置边框样式时，边框宽度与边框颜色将不会生效。

### 边框宽度

边框宽度支持数字和单位，数字部分可以通过直接输入或拖动滑块输入，支持的单位包括:

- px<sup><a href="#ref4">[4]</a></sup>: 像素，对于普通的屏幕，通常是一个设备像素（点）
- pt<sup><a href="#ref5">[5]</a></sup>: 磅（point）
- em<sup><a href="#ref6">[6]</a></sup>: 元素字体大小值
- vh<sup><a href="#ref7">[7]</a></sup>: 相对于视口高度的百分比
- vw<sup><a href="#ref8">[8]</a></sup>: 相对于视口宽度的百分比

默认单位为 px，您也可以手动输入其他单位<sup><a href="#ref9">[9]</a></sup>。

### 边框颜色

点击边框颜色块将弹出颜色选择器，您可以使用调色盘，取色器或颜色代码来选择颜色。

颜色代码模式允许切换，目前支持

- RGB(A)
- HSL(A)
- HEX(A)

## 高级模式

在高级模式下，您可以添加图片作为边框<sup><a href="#ref10">[10]</a></sup>以获得更加丰富的显示效果。

### 选择图片

点击选择图片按钮将弹出项目的图片列表，您可以在这里选择图片或添加新的图片。

### 调整裁切

选择完图片后，您可以调整裁切来按照期望的模式分割边框图片。在[配置样式](./edit-style)中我们已经使用过它了，各区域的划分模式如下<sup><a href="#ref11">[11]</a></sup>：

||九宫格划分||
|-|-|-|
|边框左上角|上边框|边框右上角|
|左边框|中间区域|右边框|
|边框左下角|下边框|边框右下角|

### 设置缩放

裁切完后的图片边框大小可能与期望的不一致，您可以通过拖动 `缩放` 滑块来调整图片边框的大小，最大值为 `100%`，最小值为 `0%`。

> 不提供大于 `100%` 的值是为了避免图片放大时出现模糊或失真。

### 边框样式

在高级模式下您也可以设置边框样式，不过与普通模式不同的是，这里控制的是图片边框的显示模式。这里的可选项包括：

- 拉伸：拉伸图片以填充边框
- 基础平铺：平铺图片以填充边框
- 拉伸平铺：平铺图像，当不能整数次平铺时，根据情况放大或缩小图像
- 留白平铺：平铺图像，当不能整数次平铺时，会用空白间隙填充在图像周围（不会放大或缩小图像）

如果您希望边框图片的中间区域也显示在背景中，可以勾选 `内部显示` 选项。

## **参考资料**

<span id="ref1">[1]</span> [MDN border-style](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/border-style)
<span id="ref2">[2]</span> [MDN border-width](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/border-width)
<span id="ref3">[3]</span> [MDN border-color](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/border-color)
<span id="ref4">[4]</span> [MDN length unit px](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#px)
<span id="ref5">[5]</span> [MDN length unit pt](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#pt)
<span id="ref6">[6]</span> [MDN length unit em](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#em)
<span id="ref7">[7]</span> [MDN length unit vh](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vh)
<span id="ref8">[8]</span> [MDN length unit vw](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#vw)
<span id="ref9">[9]</span> [MDN length](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length)
<span id="ref10">[10]</span> [MDN border-image](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/border-image)
<span id="ref11">[11]</span> [MDN border-image-slice](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Properties/border-image-slice)