<!-- * SCRIPT -->
<script setup lang="ts">
import logoLight from "@/assets/images/logo-light.svg";
import ButtonComponent from "./UI/ButtonComponent.vue";
</script>

<!-- * TEMPLATE -->
<template>
  <footer>
    <img :src="logoLight" alt="" />
    <ButtonComponent variant="gradient-purple">Get Started</ButtonComponent>
  </footer>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
footer {
  display: flex;
  place-items: center;
  justify-content: space-between;
  padding: 3.6rem 1.6rem;
  background: var(--blue-very-dark);

  @media screen and (min-width: 48em) {
    padding: 3.6rem 3.95rem;
  }

  @media screen and (min-width: 90em) {
    padding: 3.2rem 16.5rem;
  }

  img {
    width: 8.9rem;

    @media screen and (min-width: 90em) {
      width: 11.17rem;
    }
  }
}
</style>
