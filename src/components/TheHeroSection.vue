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

  .hero__cta {
    margin-bottom: 8rem;
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
      transform: scale(1.2);
    }
  }

  /*.hero__cta-img {
    margin: 0 auto;
    overflow: hidden;

    background-image: url("@/assets/images/image-hero-mobile.webp");
    background-size: cover;
    background-repeat: no-repeat;
    transform: scale(1.3);
    width: 32.7rem;
    height: 30.1rem;

    /*& > img {
    width: 32.7rem;
      width: 100%;
      transform: scale(1.28);
      clip-path: polygon(15% 0, 85% 0, 85% 85%, 15% 85%);
    }
  } */
}
</style>
