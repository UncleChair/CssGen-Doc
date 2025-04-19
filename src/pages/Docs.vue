<template>
  <v-container
    class="fill-height pa-0"
    fluid
  >
    <iframe
      ref="iframe"
      class="docs-iframe"
      frameborder="0"
      src="/docs/index.html"
      @load="onIframeLoad"
    />
  </v-container>
</template>

<script setup>
  import { ref, watch } from 'vue'
  import { useRoute } from 'vue-router'

  const route = useRoute()
  const iframe = ref(null)

  const onIframeLoad = () => {
    // 可以在这里添加 iframe 加载完成后的处理逻辑
    console.log('文档 iframe 加载完成')
  }

  // 监听路由变化，更新 iframe 内容
  watch(() => route.path, newPath => {
    if (newPath.startsWith('/docs') && iframe.value) {
      const docsPath = newPath.replace('/docs', '')
      iframe.value.contentWindow.location.hash = docsPath
    }
  })
</script>

<style scoped>
.docs-iframe {
  width: 100%;
  height: 100%;
  min-height: calc(100vh - 64px); /* 减去顶部导航栏的高度 */
}
</style>
