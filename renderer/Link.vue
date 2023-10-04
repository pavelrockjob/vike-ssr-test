<script lang="ts" setup>
import { usePageContext } from './usePageContext'
const pageContext = usePageContext()
console.log(pageContext)
</script>

<template>
  <a :class="{ active: pageContext.urlPathname === $attrs.href }">
    <slot />
  </a>
</template>

<style scoped>
a {
  padding: 3px 10px;
}
a.active {
  background-color: #eee;
}
</style>

