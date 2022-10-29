<!-- * SCRIPT -->
<script setup lang="ts">
import logo from "@/assets/images/logo-dark.svg";
import ButtonComponent from "./UI/ButtonComponent.vue";

// script goes here
</script>

<!-- * TEMPLATE -->
<template>
  <header>
    <img :src="logo" alt="" />
    <ButtonComponent variant="dark">Get Started</ButtonComponent>
  </header>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
header {
  display: flex;
  place-items: center;
  justify-content: space-between;
  padding: 1.6rem 1.6rem 0;
  margin-bottom: 3.8rem;

  @media screen and (min-width: 48em) {
    padding: 2.4rem 3.95rem 0;
    margin-bottom: 9.9rem;
  }

  @media screen and (min-width: 90em) {
    margin-bottom: 17.2rem;
    padding: 3.875rem 16.5rem;
  }

  img {
    width: 8.9rem;
    height: auto;

    @media screen and (min-width: 90em) {
      width: 11.117rem;
    }
  }
}
</style>
