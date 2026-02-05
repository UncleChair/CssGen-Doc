---
id: layout-component
title: Layout Component
description: Adjust message layout and display
order: 0
parent: normal-component
previous: normal-component
next: avatar-component
demos:
  - key: message-type-selector
    component: MessageTypeSelector
  - key: layout-demo
    title: Normal Settings - Layout
    component: LayoutDemo
---

# Layout Component

_Layout component corresponds to the layout option in the normal settings_

Layout components let you control how content is displayed and arranged, including which parts to show, how content is laid out, and which font to use for text. Options may vary slightly across platforms, but the core functionality remains consistent.

<!-- demo:message-type-selector -->

You can try the effect of different options below.

<!-- demo:layout-demo -->

- **Display**: Used to adjust the display status of the layer, you can toggle the specific layer display.
- **Layout**: Used to control the basic layout of content. The current layout is automatically detected and highlighted. Note that if you have changed to a special layout in advanced settings, it may not be matched here.
- **Font**: Used to set the basic font for content. If your browser supports fetching the local font list, options will appear in the font name field below after you click the "Get local font list" button. You can also enter a font name directly.