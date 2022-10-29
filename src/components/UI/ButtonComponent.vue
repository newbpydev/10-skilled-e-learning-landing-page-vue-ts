<!-- * SCRIPT -->
<script setup lang="ts">
defineProps<{
  variant: "dark" | "gradient-orange" | "gradient-purple" | "ghost";
}>();
</script>

<!-- * TEMPLATE -->
<template>
  <button :class="variant">
    <slot />
  </button>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
button {
  color: white;
  height: 4.8rem;
  border-radius: 2.8rem;
  padding: 0.9rem 2.4rem;
  font-size: var(--fs-body-s);
  font-weight: var(--fw-bold);
  cursor: pointer;

  &.dark {
    background: var(--blue-very-dark);
  }

  &.gradient-orange {
    height: 5.6rem;
    padding: 1.5rem 3.8rem;
    background: linear-gradient(
      180deg,
      var(--grad-orange) 0%,
      var(--grad-pink) 100%
    );
  }

  &.gradient-purple {
    color: white;
    height: 4.8rem;
    background: linear-gradient(
      180deg,
      var(--grad-purple) 0,
      var(--grad-pink) 100%
    );
  }

  &.ghost {
    color: var(--pink-dark);
    padding: 0;
    height: 2.8rem;
    letter-spacing: 0.1rem;
  }
}
</style>
