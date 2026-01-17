---
id: custom-styles
title: 自定义代码
description: 添加自定义 CSS 代码
parent: advance-component
order: 99
demos:
  - key: custom-styles-demo
    title: 自定义代码示例
    component: UserCssEditorDemo
    props:
      selector: .demo-custom-styles-demo
---

# 自定义代码组件

自定义代码组件允许在图层添加任意 CSS 代码，通常用于添加某些高级写法或编辑器不直接支持的属性。

<!-- demo:custom-styles-demo -->

> 为保证安全，自定义代码组件仅支持添加 CSS 属性声明，任何非相关内容将会被强制过滤。