---
id: text-styles
title: 文本样式
description: 文本样式组件提供了全面的文字外观控制能力
parent: style-guide
order: 10
demos:
  - key: text-color
    title: 文本颜色示例
    component: TextColor
    props:
      selector: .demo-text-color
  - key: text-shadow
    title: 文本阴影示例
    component: TextShadow
    props:
      selector: .demo-text-shadow
  - key: font-size
    title: 字体大小示例
    component: FontSize
    props:
      selector: .demo-font-size
  - key: font-weight
    title: 字体粗细示例
    component: FontWeight
    props:
      selector: .demo-font-weight
---

# 文本样式组件

文本样式组件提供了全面的文字外观控制能力。

## TextColor - 文本颜色

`TextColor` 组件用于设置文本的颜色。

### 功能特性

- 🎨 颜色选择器界面
- 支持 RGB、HEX、RGBA 格式
- 实时颜色预览
- 透明度控制

### 使用方法

```vue
<TextColor selector=".my-element" />
```

### Props

| 属性 | 类型 | 必填 | 默认值 | 说明 |
|------|------|------|--------|------|
| selector | String | 是 | - | CSS 选择器 |
| setDefault | Boolean | 否 | false | 是否设置默认值 |

### 示例

<!-- demo:text-color -->

---

## TextShadow - 文本阴影

`TextShadow` 组件用于为文本添加阴影效果。

### 功能特性

- 阴影宽度调节
- 阴影颜色选择
- 支持多层阴影（未来版本）

### 使用方法

```vue
<TextShadow selector=".my-element" />
```

### Props

| 属性 | 类型 | 必填 | 默认值 | 说明 |
|------|------|------|--------|------|
| selector | String | 是 | - | CSS 选择器 |
| setDefault | Boolean | 否 | false | 是否设置默认值 |

### 技术细节

组件内部使用 `cssData` 系统来管理样式数据：

```javascript
// 读取当前值
const width = cssData.getElementAttributeDetail(selector, "font", "shadowWidth");
const color = cssData.getElementAttributeDetail(selector, "font", "shadowColor");

// 更新值
cssData.setAttributeValue(selector, "font", "shadowWidth", newValue);
cssData.setAttributeValue(selector, "font", "shadowColor", newColor);
```

### 示例

<!-- demo:text-shadow -->

---

## FontSize - 字体大小

`FontSize` 组件用于调整文本的字体大小。

### 功能特性

- 数字输入控制
- 单位支持（px、em、rem 等）
- 最小/最大值限制

### 使用方法

```vue
<FontSize selector=".my-element" />
```

### 示例

<!-- demo:font-size -->

---

## FontWeight - 字体粗细

`FontWeight` 组件用于设置文本的粗细程度。

### 可选值

- **100-300**: 细体
- **400**: 正常
- **500-600**: 中粗
- **700**: 粗体
- **800-900**: 超粗

### 示例

<!-- demo:font-weight -->

---

## FontFamily - 字体族

`FontFamily` 组件用于选择文本的字体。

### 内置字体

- 系统字体
- 网络字体
- 自定义字体

### 字体加载

组件支持动态加载 Google Fonts 和其他网络字体。

---

## 最佳实践

### 1. 颜色对比度

确保文本颜色与背景色有足够的对比度，以保证可读性。

### 2. 字体大小

- 正文：建议 14-16px
- 标题：建议 20-32px
- 小字：建议不小于 12px

### 3. 阴影使用

- 不要过度使用阴影
- 阴影宽度建议 1-3px
- 使用半透明黑色以获得自然效果

---

> 📌 **注意**：所有文本样式组件都需要传入有效的 `selector` 属性才能正常工作。

