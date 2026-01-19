---
id: pseudo-element
title: 前/后置附加图层
description: 添加额外装饰图层
parent: advance-component
previous: custom-styles
order: 14
demos:
  - key: pseudo-element
    title: 前/后置附加图层示例
    component: PseudoElement
    sticky: true
    props:
      unique: true
---

# 前/后置附加图层

_在图层前面或后面添加额外的装饰层，用于实现特殊的装饰效果。_

<!-- demo:pseudo-element -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

前/后置附加图层本质上是一个额外添加的图层，除了一些默认属性外和基本的图层没有太大区别，您可以像设置普通图层一样调整它们。

需要注意的是，附加图层默认是内嵌在图层内部的，您可以先通过添加 `定位` 组件来调整附加图层的位置，然后通过设置 `宽度` 和 `高度` 来调整附加图层的大小（前提是先设置 `显示` 方式为非 `同行`）。

附加图层会有一个额外属性 `内容文字`，您可以在这里输入任何想要显示的文字。