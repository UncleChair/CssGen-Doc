---
id: custom-styles
title: Custom CSS
description: Add any advanced CSS code
parent: advance-component
previous: transform-styles
next: pseudo-element
order: 13
demos:
  - key: custom-styles-demo
    title: Custom CSS Example
    component: UserCssEditorDemo
    props:
      selector: .demo-custom-styles-demo
---

# Custom CSS Component

Custom CSS component allows adding any CSS code to the layer, usually used to add some advanced styles or properties that the editor does not directly support.

<!-- demo:custom-styles-demo -->

> To ensure security, the custom CSS component only supports adding CSS property declarations, any non-related content will be forcibly filtered.