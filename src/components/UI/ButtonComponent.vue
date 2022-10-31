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
  z-index: 5;

  @media screen and (min-width: 90em) {
    font-size: 1.8rem;
  }

  &.dark {
    background: var(--blue-very-dark);
    transition: all 0.3s ease-out;

    &:hover {
      background: var(--blue-light);
    }

    /*@media screen and (min-width: 48em) {
      font-size: 1.8rem;
      padding: 1.4rem 3.2rem;
    } */

    @media screen and (min-width: 90em) {
      height: 5.6rem;
      font-size: 1.8rem;
      padding: 1.4rem 3.2rem;
    }
  }

  &.gradient-orange {
    height: 5.6rem;
    padding: 1.5rem 3.8rem;
    background: linear-gradient(
      180deg,
      var(--grad-orange) 0%,
      var(--grad-pink) 100%
    );
    transition: background 0.3s ease;

    &:hover {
      background: linear-gradient(
          0deg,
          rgba(255, 255, 255, 0.5),
          rgba(255, 255, 255, 0.5)
        ),
        linear-gradient(180deg, #ff6f48 0%, #f02aa6 100%);
    }

    @media screen and (min-width: 90em) {
      height: 6.3rem;
      padding: 2rem 3.2rem;
      border-radius: 3.15rem;
    }
  }

  &.gradient-purple {
    color: white;
    height: 4.8rem;
    background: linear-gradient(
      180deg,
      var(--grad-purple) 0,
      var(--grad-pink) 100%
    );
    transition: all 0.3s ease-out;

    &:hover {
      background: linear-gradient(
          0deg,
          rgba(255, 255, 255, 0.5),
          rgba(255, 255, 255, 0.5)
        ),
        linear-gradient(180deg, #4851ff -54.32%, #f02aa6 100%);
    }

    @media screen and (min-width: 90em) {
      height: 5.6rem;
      padding: 1.4rem 3.2rem;
      font-size: 1.8rem;
    }
  }

  &.ghost {
    color: var(--pink-dark);
    padding: 0;
    height: 2.8rem;
    letter-spacing: 0.1rem;
    transition: all 0.3s ease;

    &:hover {
      color: #ffa7c3;
    }

    @media screen and (min-width: 48em) {
      font-size: 1.8rem;
      letter-spacing: 0;
    }
  }
}
</style>
