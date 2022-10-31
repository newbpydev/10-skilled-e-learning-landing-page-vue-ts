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

    <div class="hero__cta-img-container">
      <picture>
        <source
          media="(min-width: 89em)"
          srcset="@/assets/images/image-hero-desktop.webp"
        />
        <source
          media="(min-width: 48em)"
          srcset="@/assets/images/image-hero-tablet.webp"
        />
        <source
          media="(min-width: 23.43em)"
          srcset="@/assets/images/image-hero-mobile.webp"
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
  margin: 0 1.6rem;
  position: relative;

  @media screen and (min-width: 48em) {
    flex-direction: row;
    margin: 0 0 0 3.96rem;
  }

  @media screen and (min-width: 90em) {
    margin: 0 0 0 16.5rem;
  }

  .hero__cta {
    margin-bottom: 38.8rem;

    @media screen and (min-width: 48em) {
      width: 50%;
      min-width: 39.8rem;
      margin-bottom: 18.3rem;
    }

    @media screen and (min-width: 90em) {
      width: 45.7rem;
      margin-bottom: 22.6rem;
    }
    .hero__heading {
      font-size: var(--fs-heading-l);
      font-weight: var(--fw-x-bold);
      line-height: 5rem;
      margin-bottom: 2.8rem;

      @media screen and (min-width: 90em) {
        font-size: var(--fs-heading-xl);
        line-height: 7.056rem;
        margin-bottom: 2.9rem;
      }
    }

    .hero__message {
      line-height: 2.6rem;
      color: var(--blue-greyish);
      width: 100%;
      margin-bottom: 2.4rem;

      @media screen and (min-width: 48em) {
        width: 39.8rem;
      }

      @media screen and (min-width: 90em) {
        margin-bottom: 4rem;
        font-size: 1.8rem;
        width: 44.5rem;
        line-height: 2.8rem;
      }
    }
  }

  .hero__cta-img-container {
    /* overflow: hidden; */

    @media screen and (min-width: 48em) {
      overflow-x: clip;
    }

    @media screen and (min-width: 90em) {
    }

    & img {
      max-width: none;
      position: absolute;
      display: block;
      top: 31rem;
      left: -4.6rem;
      width: 43.7rem;
      /* height: 93.692rem; */
      height: auto;

      @media screen and (min-width: 48em) {
        top: -26.6rem;
        left: 33rem;
        width: 69.863rem;
      }

      @media screen and (min-width: 90em) {
        top: -41.6rem;
        left: 46.7rem;

        width: 104.1rem;
        transform: translate(10rem, 2rem);
      }
    }
  }
}
</style>
