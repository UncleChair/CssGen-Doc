---
id: shadow-styles
title: 阴影样式
description: 为图层添加阴影效果
parent: advance-component
previous: display-styles
next: transform-styles
order: 11
demos:
  - key: shadow-editor
    title: 阴影示例
    component: ShadowEditor
    sticky: true
    props:
      unique: true
---

# 阴影样式组件

_为图层添加阴影效果，增强视觉层次感和立体感。_

<!-- demo:shadow-editor -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

阴影列表中可以添加多个阴影效果，每个阴影效果可以设置阴影相关的属性。

## 水平偏移

阴影相对于图层的的水平偏移距离，支持数字输入，只支持单位 `px`。

## 垂直偏移

阴影相对于图层的的垂直偏移距离，支持数字输入，只支持单位 `px`。

## 模糊距离

用以控制阴影的扩散范围，支持数字输入，只支持正数和单位 `px`。

## 阴影大小

用以控制阴影的大小，支持数字输入，只支持正数和单位 `px`。

## 阴影颜色

阴影的颜色，支持颜色选择器。点击阴影颜色块将弹出颜色选择器，您可以使用调色盘，取色器或颜色代码来选择颜色。

颜色代码模式允许切换，目前支持

- RGB(A)
- HSL(A)
- HEX(A)

## 内部阴影

勾选 `内部阴影` 选项后，阴影将会被绘制在图层的内部，而不是外部。