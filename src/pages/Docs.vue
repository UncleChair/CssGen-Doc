<template>
  <v-container
    class="fill-height pa-0"
    fluid
  >
    <iframe
      class="docs-iframe"
      frameborder="0"
      src="/docs/index.html"
      @load="onIframeLoad"
    />
  </v-container>
</template>

<script setup>
  const onIframeLoad = () => {
    // 可以在这里添加 iframe 加载完成后的处理逻辑
    console.log('文档 iframe 加载完成')
  }
</script>

<style scoped>
.docs-iframe {
  width: 100%;
  height: 100%;
  min-height: calc(100vh - 64px); /* 减去顶部导航栏的高度 */
}
</style>
