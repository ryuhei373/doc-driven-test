<script setup lang="ts">
const { toc } = useContent()
</script>
<template>
  <div>
    <h2>目次</h2>
    <ul v-if="toc && toc.links">
      <li v-for="link in toc.links" :key="link.text">
        <a
          :href="`#${link.id}`"
        >
          {{ link.text }}
        </a>
      </li>
    </ul>
  </div>
</template>