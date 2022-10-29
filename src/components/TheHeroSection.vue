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
      <ButtonComponent variant="gradient-orange">Get Started</ButtonComponent>
    </div>

    <div class="hero__cta-img-container" role="img">
      <picture>
        <source
          media="(min-width: 40rem)"
          srcset="@/assets/images/image-hero-mobile.png"
        />
        <img
          :src="heroImage"
          alt="image of the number of member and course hours"
        />
      </picture>
    </div>
  </section>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  margin-bottom: 1.6rem;

  .hero__cta {
    margin-bottom: 7.1rem;
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
  }

  .hero__cta-img-container {
    min-width: 32.7rem;
    overflow: hidden;

    & img {
      transform: scale(1.27);
    }
  }
}
</style>
