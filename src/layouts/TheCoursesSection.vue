<!-- * SCRIPT -->
<script setup lang="ts">
// script goes here
</script>

<!-- * TEMPLATE -->
<template>
  <section class="courses-section container">
    <slot />
  </section>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
.courses-section {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 1.6rem;
  margin-bottom: 8rem;

  @media screen and (min-width: 48em) {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
    row-gap: 3.2rem;
    margin-bottom: 8.6rem;
  }
}
</style>
