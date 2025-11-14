---
id: border-styles
title: 边框样式
description: 边框样式组件提供了完整的边框定制能力
parent: style-guide
order: 1
demos:
  - key: border-editor
    title: 边框示例
    component: BorderEditor
    props:
      selector: .demo-border-editor
  - key: border-basic
    title: 基础边框示例
    component: Border
    props:
      selector: .demo-border
  - key: border-radius
    title: 简单圆角示例
    component: BorderRadiusSimple
    props:
      selector: .demo-border-radius
  - key: box-shadow
    title: 盒阴影示例
    component: BoxShadow
    props:
      selector: .demo-box-shadow
---

# 边框样式组件

边框样式组件提供了完整的边框定制能力。

## Border - 基础边框

`Border` 组件用于设置元素的边框样式。

### 功能特性

- 边框宽度控制
- 边框颜色选择
- 边框样式选择
- 四边独立控制

### 边框样式类型

| 样式 | 效果 | 说明 |
|------|------|------|
| `solid` | ──── | 实线 |
| `dashed` | ─ ─ ─ | 虚线 |
| `dotted` | ······ | 点线 |
| `double` | ═══ | 双线 |
| `groove` | 凹槽 | 3D 凹槽效果 |
| `ridge` | 凸起 | 3D 凸起效果 |
| `inset` | 内嵌 | 3D 内嵌效果 |
| `outset` | 外凸 | 3D 外凸效果 |

### 使用方法

```vue
<Border selector=".my-element" />
```

### 交互式演示

通过下面的交互式演示，你可以实时调整边框的各种属性，并在右侧预览区看到效果：

<!-- demo:border-editor -->

---

## BorderRadiusSimple - 简单圆角

`BorderRadiusSimple` 组件提供了统一的圆角设置。

### 功能特性

- 单一数值控制
- 四个角统一圆角
- 快速设置

### 常用值

- `0px` - 直角
- `4px` - 轻微圆角
- `8px` - 中等圆角
- `16px` - 明显圆角
- `50%` - 完全圆形（正方形元素）

### 交互式演示

尝试调整圆角大小，看看不同数值的效果：

<!-- demo:border-radius -->

---

## BorderRadiusAdvance - 高级圆角

`BorderRadiusAdvance` 组件提供了更精细的圆角控制。

### 功能特性

- 四个角独立控制
- 每个角的水平/垂直半径独立设置
- 创造复杂的圆角效果

### 四角控制

```
┌─────────┐
│ TL   TR │  TL: top-left (左上)
│         │  TR: top-right (右上)
│         │  BL: bottom-left (左下)
│ BL   BR │  BR: bottom-right (右下)
└─────────┘
```

### 椭圆圆角

可以为每个角设置不同的水平和垂直半径：

```css
border-radius: 10px 20px 30px 40px / 40px 30px 20px 10px;
```

---

## BoxShadow - 盒阴影

`BoxShadow` 组件用于为元素添加阴影效果。

### 功能特性

- X/Y 偏移量控制
- 模糊半径调节
- 扩展半径调节
- 阴影颜色选择
- 内阴影/外阴影切换
- 多重阴影支持

### 阴影参数

```css
box-shadow: [inset] x-offset y-offset blur spread color;
```

| 参数 | 说明 | 单位 |
|------|------|------|
| inset | 可选，内阴影 | - |
| x-offset | 水平偏移 | px |
| y-offset | 垂直偏移 | px |
| blur | 模糊半径 | px |
| spread | 扩展半径 | px |
| color | 阴影颜色 | color |

### 交互式演示

通过下面的演示，你可以实时调整阴影的各个参数，创造出不同的阴影效果：

<!-- demo:box-shadow -->

### 阴影效果示例

#### 1. 轻微浮起

```css
box-shadow: 0 2px 4px rgba(0,0,0,0.1);
```

#### 2. 明显浮起

```css
box-shadow: 0 4px 8px rgba(0,0,0,0.15);
```

#### 3. 强烈浮起

```css
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
```

#### 4. 内阴影

```css
box-shadow: inset 0 2px 4px rgba(0,0,0,0.1);
```

#### 5. 发光效果

```css
box-shadow: 0 0 20px rgba(33,150,243,0.8);
```

#### 6. 多重阴影

```css
box-shadow: 
  0 2px 4px rgba(0,0,0,0.1),
  0 4px 8px rgba(0,0,0,0.1),
  0 8px 16px rgba(0,0,0,0.1);
```

---

## BorderImage - 边框图片

详见"背景样式组件"章节。

---

## 设计指南

### 1. 边框粗细

- **细边框** (1px): 适合分隔线、卡片边框
- **中等边框** (2-3px): 适合强调元素
- **粗边框** (4px+): 适合装饰性元素

### 2. 圆角大小

- **小圆角** (2-4px): 现代、专业
- **中圆角** (8-12px): 友好、柔和
- **大圆角** (16px+): 活泼、有趣
- **圆形** (50%): 头像、按钮

### 3. 阴影层次

#### 扁平设计
```css
box-shadow: none;
```

#### Material Design 层次

**Level 1** - 静止卡片
```css
box-shadow: 0 1px 3px rgba(0,0,0,0.12);
```

**Level 2** - 悬停卡片
```css
box-shadow: 0 3px 6px rgba(0,0,0,0.16);
```

**Level 3** - 浮动按钮
```css
box-shadow: 0 10px 20px rgba(0,0,0,0.19);
```

**Level 4** - 对话框
```css
box-shadow: 0 14px 28px rgba(0,0,0,0.25);
```

**Level 5** - 抽屉
```css
box-shadow: 0 19px 38px rgba(0,0,0,0.30);
```

---

## 组合效果

### 卡片样式

```css
border: 1px solid #e0e0e0;
border-radius: 8px;
box-shadow: 0 2px 4px rgba(0,0,0,0.1);
```

### 按钮样式

```css
border: none;
border-radius: 4px;
box-shadow: 0 2px 4px rgba(0,0,0,0.2);
```

### 输入框样式

```css
border: 2px solid #2196f3;
border-radius: 4px;
box-shadow: 0 0 0 4px rgba(33,150,243,0.1);
```

---

## 动画效果

### 悬停提升

```css
.element {
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: box-shadow 0.3s ease;
}

.element:hover {
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}
```

### 边框动画

```css
.element {
  border: 2px solid transparent;
  transition: border-color 0.3s ease;
}

.element:hover {
  border-color: #2196f3;
}
```

---

> 🎨 **设计提示**：边框和阴影是创造视觉层次的重要工具，但不要过度使用！

