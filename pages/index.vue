<script setup lang="ts">

import AboutSection from "~/components/AboutSection.vue";
import SimplifySection from "~/components/SimplifySection.vue";
import AppFooter from "~/components/AppFooter.vue";
</script>

<template>
  <div>
    <app-header/>
    <main>
      <main-section/>
      <about-section/>
      <carousel-section/>
      <simplify-section/>
      <app-footer/>
    </main>
  </div>
</template>

<style scoped>

</style>