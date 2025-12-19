---
id: page-guide
title: 界面指南
description: 了解编辑器界面布局和功能
order: 1
previous: quick-start
demos:
  - key: message-type-selector
    component: MessageTypeSelectorDemo
  - key: message-preview
    component: MessagePreviewDemo
  - key: operation-list
    component: OperationListDemo
  - key: user-setting
    component: UserSettingDemo
---

# 编辑器简介

_初次打开编辑器后，您会进入一个简单的流程指引来帮助您了解编辑器的功能和区块划分，建议您先完成流程指引。_

![编辑器界面](./static/editor.png)

## 区块划分

_您可以随时前往编辑器页面的对应区块进行操作。_

### 类型选择

用于选择消息的类型，您可以在此选择要调整的消息。

<!-- demo:message-type-selector -->

### 预览区域

在类型选择区域下方为当前选中类型的消息样式预览。在高级设置模式下，你也可以通过点击预览内容来选中对应的图层。

<!-- demo:message-preview -->

> 在高级设置模式下，点击对应的图层也会有闪烁的红色边框渲染在对应的图层上。

### 编辑区域

界面的右侧为编辑区域，您可以在此进行样式编辑和消息内容设置。预览区域会根据您设置的内容进行实时更新。

#### 样式设置

样式设置区域包含了编辑器的绝大部分操作内容，你可以在这里自由地进行样式编辑。

<!-- demo:operation-list -->

#### 消息内容设置

消息内容设置区域能够配置预览中的显示内容，您可以在这里进行各种操作以预览样式在不同情况下的显示效果。

<!-- demo:user-setting -->

_消息内容设置中的内容不会保存到配置中，每次进入编辑器都会重置。_

### 系统设置

右上角为系统设置区域，您可以在此进行：

- 教程重放
- 云同步
- 主题切换
- 语言切换
- 快捷键设置
- 项目设置