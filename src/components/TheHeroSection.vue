<!-- * SCRIPT -->
<script setup lang="ts">
import heroImage from "@/assets/images/image-hero-mobile.png";
import ButtonComponent from "@/components/UI/ButtonComponent.vue";
</script>

<!-- * TEMPLATE -->
<template>
  <section class="hero">
    <div class="hero__cta">
      <h1 class="hero__heading">Maximize skill, minimize budget</h1>
      <p class="hero__message">
        Our modern courses across a range of in-demand skills will give you the
        knowledge you need to live the life you want.
      </p>
      <ButtonComponent type="gradient-orange">Get Started</ButtonComponent>
    </div>

    <div class="hero__cta-img">
      <img
        :src="heroImage"
        alt="image of the number of member and course hours"
      />
    </div>
  </section>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;

  .hero__cta {
    margin-bottom: 8rem;
  }

  .hero__heading {
    font-size: var(--fs-heading-l);
    font-weight: var(--fw-x-bold);
    line-height: 5rem;
    margin-bottom: 2.6rem;
  }

  .hero__message {
    line-height: 2.6rem;
    color: var(--blue-greyish);
    width: 100%;
    margin-bottom: 2.4rem;
  }

  .hero__cta-img > img {
    width: 32.7rem;
    transform: scale(1.35);
  }
}
</style>
