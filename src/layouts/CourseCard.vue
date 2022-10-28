<!-- * SCRIPT -->
<script setup lang="ts">
// script goes here
</script>

<!-- * TEMPLATE -->
<template>
  <article class="course-card">
    <div class="course-card__icon">
      <slot name="icon" />
    </div>

    <h3 class="course-card__heading">
      <slot name="heading" />
    </h3>

    <p class="course-card__text">
      <slot name="text" class="course-card__text" />
    </p>

    <!-- TODO: add button here -->
  </article>
</template>

<!-- * STYLE -->
<style scoped>
/* styles go here */
</style>
