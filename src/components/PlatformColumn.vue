<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  items: {
    type: Array,
    required: true
  }
})

const typeLabel = {
  global: '国际',
  local: '国内',
  tool: '工具',
  app: '软件'
}
</script>

<template>
  <section class="column">
    <h2 class="column-title">{{ title }}</h2>
    <ul class="card-list">
      <li v-for="item in items" :key="item.name">
        <a class="card" :class="`type-${item.type}`" :href="item.url" target="_blank" rel="noreferrer">
          <span class="dot" aria-hidden="true"></span>
          <span class="name">{{ item.name }}</span>
          <span class="badge">{{ typeLabel[item.type] || '平台' }}</span>
          <span class="arrow" aria-hidden="true">↗</span>
        </a>
      </li>
    </ul>
  </section>
</template>
