<!-- * SCRIPT -->
<script setup lang="ts">
import DefaultLayout from "@/layouts/DefaultLayout.vue";
import TheHeroSection from "./components/TheHeroSection.vue";
import ButtonComponent from "./components/UI/ButtonComponent.vue";

// Icons
import animation from "@/assets/images/icon-animation.svg";
import business from "@/assets/images/icon-business.svg";
import crypto from "@/assets/images/icon-crypto.svg";
import design from "@/assets/images/icon-design.svg";
import photography from "@/assets/images/icon-photography.svg";
import CourseCard from "./layouts/CourseCard.vue";
</script>

<!-- * TEMPLATE -->
<template>
  <DefaultLayout>
    <TheHeroSection />

    <CourseCard :icon-src="animation">
      <template #heading>Animation</template>
      <template #text>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quia dolorum
        excepturi exercitationem?</template
      >
      <template #button-text>Get Started</template>
    </CourseCard>

    <CourseCard>
      <template #title>A different card</template>
    </CourseCard>
    Check out our most popular courses! Animation Learn the latest animation
    techniques to create stunning motion design and captivate your audience. Get
    Started Design Create beautiful, usable interfaces to help shape the future
    of how the web looks. Get Started Photography Explore critical fundamentals
    like lighting, composition, and focus to capture exceptional photos. Get
    Started Crypto All you need to know to get started investing in crypto. Go
    from beginner to advanced with this 54 hour course. Get Started Business A
    step-by-step playbook to help you start, scale, and sustain your business
    without outside investment. Get Started Get Started
  </DefaultLayout>
</template>

<!-- * STYLE -->
<style scoped></style>
