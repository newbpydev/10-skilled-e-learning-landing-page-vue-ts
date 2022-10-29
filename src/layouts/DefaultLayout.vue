<!-- * SCRIPT -->
<script setup lang="ts">
import TheFooter from "@/components/TheFooter.vue";
import TheHeader from "@/components/TheHeader.vue";

// script goes here
</script>

<!-- * TEMPLATE -->
<template>
  <TheHeader />

  <main>
    <slot></slot>
  </main>

  <TheFooter />
</template>

<!-- * STYLE -->
<style scoped lang="scss"></style>
