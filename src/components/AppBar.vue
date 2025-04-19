<template>
  <v-app-bar
    app
    color="primary"
    density="compact"
  >
    <v-app-bar-title>CssGen</v-app-bar-title>

    <v-spacer />

    <v-btn
      v-for="item in items"
      :key="item.title"
      :to="item.to"
      variant="text"
    >
      {{ item.title }}
    </v-btn>
  </v-app-bar>
</template>

<script setup>
  const items = [
    {
      title: '首页',
      to: '/',
    },
    {
      title: '文档',
      to: '/docs',
    },
  ]
</script>
