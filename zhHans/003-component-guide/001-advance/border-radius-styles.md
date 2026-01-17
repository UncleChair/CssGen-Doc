---
id: border-radius-styles
title: 圆角样式
description: 定制圆角样式
parent: advance-component
previous: opacity-styles
order: 6
demos:
  - key: border-radius-editor
    title: 边框圆角示例
    component: BorderRadiusEditor
---

# 边框圆角样式组件

_边框圆角指的是图层的边框圆角大小。_

<!-- demo:border-radius-editor -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

边框圆角样式组件目前仅支持 `px`<sup><a href="#ref1">[1]</a></sup> 单位。

## 整体调整

在整体调整模式下，您可以同时设置四个方向的圆角大小，可以通过直接输入或拖动滑块输入，只支持正数。

## 单个调整

在单个调整模式下，您可以单独设置四个方向（左上、右上、右下、左下）的圆角大小，支持的数字和单位与整体调整模式相同。

## **参考资料**

<span id="ref1">[1]</span> [MDN length unit px](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference/Values/length#px)