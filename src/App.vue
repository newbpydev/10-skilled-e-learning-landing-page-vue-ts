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
import TheCoursesSection from "./layouts/TheCoursesSection.vue";
</script>

<!-- * TEMPLATE -->
<template>
  <DefaultLayout>
    <!-- @ Hero Section -->
    <TheHeroSection />

    <!-- @ Courses Section -->
    <TheCoursesSection>
      <!-- # title card -->
      <CourseCard>
        <template #title>Check out our most popular courses!</template>
      </CourseCard>

      <!-- # Animation card -->
      <CourseCard :icon-src="animation">
        <template #heading>Animation</template>
        <template #text>
          Learn the latest animation techniques to create stunning motion design
          and captivate your audience.
        </template>
        <template #button-text>Get Started</template>
      </CourseCard>

      <!-- # Design card -->
      <CourseCard :icon-src="design">
        <template #heading>Design</template>
        <template #text>
          Create beautiful, usable interfaces to help shape the future of how
          the web looks.
        </template>
        <template #button-text>Get Started</template>
      </CourseCard>

      <!-- # Photography card -->
      <CourseCard :icon-src="photography">
        <template #heading>Photography</template>
        <template #text>
          Explore critical fundamentals like lighting, composition, and focus to
          capture exceptional photos.
        </template>
        <template #button-text>Get Started</template>
      </CourseCard>

      <!-- # Crypto card -->
      <CourseCard :icon-src="crypto">
        <template #heading>Crypto</template>
        <template #text>
          All you need to know to get started investing in crypto. Go from
          beginner to advanced with this 54 hour course.
        </template>
        <template #button-text>Get Started</template>
      </CourseCard>

      <!-- # Business card -->
      <CourseCard :icon-src="business">
        <template #heading>Business</template>
        <template #text>
          A step-by-step playbook to help you start, scale, and sustain your
          business without outside investment.
        </template>
        <template #button-text>Get Started</template>
      </CourseCard>
    </TheCoursesSection>
  </DefaultLayout>
</template>

<!-- * STYLE -->
<style scoped></style>
