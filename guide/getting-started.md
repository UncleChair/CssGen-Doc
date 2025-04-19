# 快速开始

本文档将帮助您快速开始使用 CssGen。

## 安装

```bash
npm install cssgen
```

## 使用

```javascript
import { createApp } from 'vue'
import CssGen from 'cssgen'
import App from './App.vue'

const app = createApp(App)
app.use(CssGen)
app.mount('#app')
```

## 示例

```vue
<template>
  <div>
    <css-gen-button>按钮</css-gen-button>
  </div>
</template>

<script setup>
import { CssGenButton } from 'cssgen'
</script> 