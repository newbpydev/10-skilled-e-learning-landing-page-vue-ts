<!-- * SCRIPT -->
<script setup lang="ts">
import ButtonComponent from "@/components/UI/ButtonComponent.vue";

interface Props {
  iconSrc?: string;
}

defineProps<Props>();
</script>

<!-- * TEMPLATE -->
<template>
  <!-- @ if iconSrc -->
  <article class="course-card" v-if="iconSrc">
    <!-- # icon -->
    <div class="course-card__icon" v-if="iconSrc">
      <img class="course-card__icon-img" :src="iconSrc" aria-hidden="true" />
    </div>

    <!-- # heading -->
    <h3 class="course-card__heading">
      <slot name="heading" />
    </h3>

    <!-- # text -->
    <p class="course-card__text">
      <slot name="text" />
    </p>

    <!-- # button -->
    <div class="course-card__button">
      <ButtonComponent variant="ghost">
        <slot name="button-text" />
      </ButtonComponent>
    </div>
  </article>

  <!-- @ else -->
  <article class="course-card-alt" v-else>
    <h2 class="course-card-alt__title">
      <slot name="title" />
    </h2>
  </article>
</template>

<!-- * STYLE -->
<style scoped lang="scss">
/* normal card */
.course-card {
  background: var(--white-pure);
  border-radius: var(--border-radius-mobile-tablet);
  position: relative;
  padding: 5.6rem 2.8rem 3.2rem;
  margin-top: 2.4rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  @media screen and (min-width: 48em) {
    padding: 5.6rem 2.2rem 3.2rem 3.2rem;
  }

  @media screen and (min-width: 90em) {
    padding: 6.4rem 3.2rem 4rem;
  }

  &__icon {
    &-img {
      position: absolute;
      top: -2.3rem;
      height: 5.6rem;
      width: 5.6rem;
    }
  }

  &__heading {
    font-size: 2rem;
    font-weight: var(--fw-x-bold);
    margin-bottom: 1.6rem;

    @media screen and (min-width: 90em) {
      font-size: 2.4rem;
      margin-bottom: 2.4rem;
    }
  }

  &__text {
    color: var(--blue-greyish);
    line-height: 2.6rem;
    margin-bottom: 2.4rem;
    flex-grow: 1;

    @media screen and (min-width: 90em) {
      font-size: 1.8rem;
      line-height: 2.8rem;
    }
  }

  &__button {
  }
}

/* title card */
.course-card-alt {
  margin-top: 2.4rem;

  &__title {
    font-size: var(--fs-heading-s);
    font-weight: var(--fw-x-bold);
    color: var(--white-pure);
    border-radius: var(--border-radius-mobile-tablet);
    padding: 2.8rem 2.8rem 3rem;
    line-height: 3rem;
    background: linear-gradient(
      180deg,
      var(--grad-orange) 0%,
      var(--grad-pink) 100%
    );

    @media screen and (min-width: 48em) {
      padding: 5.6rem 3.2rem 13.9rem;
      line-height: 3.2rem;
      height: 100%;
    }

    @media screen and (min-width: 90em) {
      font-size: var(--fs-heading-m);
      line-height: 4rem;
      padding: 6.4rem 3.2rem 13.8rem;
    }
  }
}
</style>
