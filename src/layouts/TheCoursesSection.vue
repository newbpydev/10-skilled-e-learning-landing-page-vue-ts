<!-- * SCRIPT -->
<script setup lang="ts">
// script goes here
</script>

<!-- * TEMPLATE -->
<template>
  <section class="courses-section">
    <slot />
  </section>
</template>

<!-- * STYLE -->
<style scoped>
.courses-section {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 1.6rem;
}
</style>
