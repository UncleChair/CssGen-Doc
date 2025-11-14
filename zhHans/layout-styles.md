---
id: layout-styles
title: 布局样式
description: 布局样式组件帮助你控制元素的显示和排列方式
parent: style-guide
order: 40
demos:
  - key: display
    title: 显示方式示例
    component: Display
    props:
      selector: .demo-display
  - key: flex-direction
    title: Flex 方向示例
    component: FlexDirection
    props:
      selector: .demo-flex-direction
  - key: justify-content
    title: 主轴对齐示例
    component: JustifyContent
    props:
      selector: .demo-justify-content
  - key: align-items
    title: 交叉轴对齐示例
    component: AlignItems
    props:
      selector: .demo-align-items
  - key: overflow
    title: 溢出控制示例
    component: Overflow
    props:
      selector: .demo-overflow
---

# 布局样式组件

布局样式组件帮助你控制元素的显示和排列方式。

## Display - 显示方式

`Display` 组件用于控制元素的显示类型。

### 显示模式

| 模式 | 说明 | 适用场景 |
|------|------|----------|
| `block` | 块级元素 | 独占一行的元素（如标题、段落） |
| `inline` | 行内元素 | 在同一行内的元素（如链接、文字） |
| `inline-block` | 行内块元素 | 同行但可设置宽高 |
| `flex` | 弹性盒子 | 现代布局方案 |
| `grid` | 网格布局 | 二维布局系统 |
| `none` | 隐藏元素 | 完全不显示 |

### 使用方法

```vue
<Display selector=".my-element" />
```

### 交互式演示

<!-- demo:display -->

---

## Flex 布局

Flex 布局是现代 CSS 布局的核心技术，提供了强大的对齐和分布能力。

### FlexDirection - 主轴方向

控制 Flex 容器内子元素的排列方向。

#### 可选值

- **row** (→): 从左到右水平排列
- **row-reverse** (←): 从右到左水平排列
- **column** (↓): 从上到下垂直排列
- **column-reverse** (↑): 从下到上垂直排列

```vue
<FlexDirection selector=".flex-container" />
```

#### 交互式演示

<!-- demo:flex-direction -->

### JustifyContent - 主轴对齐

控制子元素在主轴上的对齐方式。

#### 对齐方式

```
flex-start (起始对齐)
[1][2][3]          空

center (居中对齐)
   空   [1][2][3]   空

flex-end (结束对齐)
          空   [1][2][3]

space-between (两端对齐)
[1]     空     [2]     空     [3]

space-around (环绕对齐)
  空  [1]  空  [2]  空  [3]  空

space-evenly (均分对齐)
   空   [1]   空   [2]   空   [3]   空
```

```vue
<JustifyContent selector=".flex-container" />
```

#### 交互式演示

<!-- demo:justify-content -->

### AlignItems - 交叉轴对齐

控制子元素在交叉轴上的对齐方式。

#### 对齐方式

- **flex-start**: 交叉轴起点对齐
- **flex-end**: 交叉轴终点对齐
- **center**: 交叉轴居中对齐
- **baseline**: 基线对齐
- **stretch**: 拉伸填充

```vue
<AlignItems selector=".flex-container" />
```

#### 交互式演示

<!-- demo:align-items -->

---

## Flex 布局实战

### 水平居中

```css
.container {
  display: flex;
  justify-content: center;
}
```

### 垂直居中

```css
.container {
  display: flex;
  align-items: center;
}
```

### 完全居中

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### 两端对齐

```css
.container {
  display: flex;
  justify-content: space-between;
}
```

### 等距排列

```css
.container {
  display: flex;
  justify-content: space-evenly;
}
```

### 垂直布局

```css
.container {
  display: flex;
  flex-direction: column;
}
```

### 反向排列

```css
.container {
  display: flex;
  flex-direction: row-reverse;
}
```

---

## Overflow - 溢出控制

`Overflow` 组件控制内容溢出容器时的显示方式。

### 溢出模式

| 模式 | 说明 | 效果 |
|------|------|------|
| `visible` | 可见 | 溢出内容正常显示 |
| `hidden` | 隐藏 | 裁剪溢出内容 |
| `scroll` | 滚动条 | 始终显示滚动条 |
| `auto` | 自动 | 需要时显示滚动条 |

### 交互式演示

<!-- demo:overflow -->

### 使用场景

#### 1. 裁剪溢出

```css
overflow: hidden;
```

用于隐藏超出容器的内容。

#### 2. 可滚动容器

```css
overflow: auto;
```

创建可滚动的内容区域。

#### 3. 文字省略

```css
overflow: hidden;
text-overflow: ellipsis;
white-space: nowrap;
```

单行文本溢出显示省略号。

---

## 布局最佳实践

### 1. Flexbox vs Grid

**使用 Flexbox**：
- 一维布局（行或列）
- 内容驱动的布局
- 小规模布局

**使用 Grid**：
- 二维布局（行和列）
- 布局驱动的设计
- 大规模布局

### 2. 响应式布局

```css
.container {
  display: flex;
  flex-wrap: wrap;
}

.item {
  flex: 1 1 300px; /* 最小宽度 300px */
}
```

### 3. 常见布局模式

#### Header-Content-Footer

```css
.page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.header, .footer {
  flex: 0 0 auto;
}

.content {
  flex: 1 0 auto;
}
```

#### 侧边栏布局

```css
.layout {
  display: flex;
}

.sidebar {
  flex: 0 0 250px;
}

.main {
  flex: 1;
}
```

#### 卡片网格

```css
.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 calc(33.333% - 20px);
  min-width: 250px;
}
```

---

## 调试技巧

### 1. 可视化 Flex 容器

```css
.flex-container {
  border: 2px solid red;
}

.flex-item {
  border: 1px solid blue;
}
```

### 2. 使用浏览器开发工具

现代浏览器提供了 Flexbox 可视化工具：
- Chrome DevTools - Flexbox 检查器
- Firefox DevTools - Flex 容器高亮
- Safari Web Inspector - Flex 布局工具

### 3. 常见问题

#### 元素不居中？

检查：
- 容器是否设置了 `display: flex`
- 是否同时设置了 `justify-content` 和 `align-items`
- 容器是否有足够的高度

#### 元素被压缩？

使用 `flex-shrink: 0` 防止元素缩小：

```css
.item {
  flex-shrink: 0;
}
```

#### 元素间距不均匀？

使用 `gap` 属性（推荐）：

```css
.container {
  display: flex;
  gap: 20px;
}
```

---

## 参考资源

- [CSS Flexbox 完全指南](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [MDN Flexbox 文档](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [Flexbox Froggy](https://flexboxfroggy.com/) - 交互式学习游戏

---

> 🎯 **实践提示**：最好的学习方法是实践！使用下方的交互式演示尝试不同的布局配置。

