---
id: display-styles
title: 显示与排版样式
description: 调整图层的显示与排列方式
parent: advance-component
previous: position-styles
next: shadow-styles
order: 10
demos:
  - key: display-editor-simple
    title: 显示与排版示例
    component: DisplayEditorSimple
    sticky: true
    props:
      unique: true
---

# 显示与排版样式组件

_控制图层如何显示在页面上，以及如何排列组织它们的位置。_

<!-- demo:display-editor-simple -->

> 强制应用选项可以强制覆盖样式设置，通常在某些平台中调整无效时使用。

## 显示方式选项<sup><a href="#ref1">[1]</a></sup>

### 隐藏 (none)

让图层完全消失，不会显示在页面上，也不会占用任何空间。

### 默认 (unset)

让图层恢复到默认的显示方式，大部分情况下等同于 `换行` 的显示方式。

### 布局 (flex)

启用强大的弹性布局模式，可以灵活控制水平和垂直排版的方式。

#### 主轴方向

排版的主要方向，类似于队伍排列的方向，默认情况下是横向排列。

**选项**：
- **从左往右（row）**
- **从右往左（row-reverse）**
- **从上往下（column）**
- **从下往上（column-reverse）**

#### 主轴对齐<sup><a href="#ref2">[2]</a></sup>

控制排版在主轴方向上如何分布。

**选项**：
- **其实对齐（flex-start）**：所有图层靠在起始端
- **结束对齐（flex-end）**：所有图层靠在末端
- **居中（center）**：所有图层居中对齐
- **最大平铺（space-between）**：图层均匀分布，首尾图层贴边
- **等距平铺（space-around）**：图层均匀分布，每个图层周围分配相同的空间
- **平均平铺（space-evenly）**：图层均匀分布，每个图层之间的间隔相等

#### 交叉轴<sup><a href="#ref3">[3]</a></sup>

交叉轴是垂直于主轴的方向，如果主轴是横向，交叉轴就是纵向；反之亦然。

**选项**：
- **平铺（stretch）**：图层拉伸填满容器
- **居中（center）**：图层居中对齐
- **起始对齐（start）**：图层靠在起始端
- **结束对齐（end）**：图层靠在末端

### 换行 (block)

控制当一行/一列放不下所有图层时，是否换行。

### 同行 (inline)

让图层像文字一样排列，多个图层会紧挨着排在同一行。

## 溢出设置<sup><a href="#ref4">[4]</a></sup>

当图层内容超出容器大小时，控制是否显示溢出部分。

**显示溢出（visible）**：
- 内容会溢出显示，不会被裁剪

**隐藏溢出（hidden）**：
- 超出部分会被裁剪，不显示

## 参考资料

<span id="ref1">[1]</span> [CSS 属性 - display](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display)
<span id="ref2">[2]</span> [CSS 属性 - 主轴对齐](https://developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content)
<span id="ref3">[3]</span> [CSS 属性 - 交叉轴对齐](https://developer.mozilla.org/zh-CN/docs/Web/CSS/align-items)
<span id="ref4">[4]</span> [CSS 属性 - 溢出设置](https://developer.mozilla.org/zh-CN/docs/Web/CSS/overflow)