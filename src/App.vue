<script setup>
import PlatformColumn from './components/PlatformColumn.vue'
import { platformColumns } from './data/platforms'

const total = platformColumns.reduce((count, column) => count + column.items.length, 0)
</script>

<template>
  <main class="page">
    <div class="panel">
      <header class="hero">
        <div>
          <h1>Ssuperjee的世界</h1>
          <p>/ 开放平台 · 官方链接</p>
        </div>
        <span class="count">{{ total }} 个直达入口</span>
      </header>

      <p class="tip">优先整理官方站点与开放平台，快速找到可用模型、工具与企业接入入口。</p>

      <div class="columns">
        <PlatformColumn
          v-for="column in platformColumns"
          :key="column.title"
          :title="column.title"
          :items="column.items"
        />
      </div>
    </div>
  </main>
</template>
