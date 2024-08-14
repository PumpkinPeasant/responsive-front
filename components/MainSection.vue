<script setup lang="ts">
import AButton from "~/components/UI/AButton.vue";
import ChartImg from '~/assets/images/illustration-intro.svg'
import EvenColumns from "~/components/UI/containers/EvenColumns.vue";
</script>

<template>
  <even-columns class="padding-block-900">
    <div>
      <h1 class="fs-primary-heading fw-bold">Bring everyone together to build better products.</h1>
      <p>Manage makes it simple for software teams to plan day-to-day tasks while keeping the larger team goals in
        view.</p>
      <a-button/>
    </div>
    <div>
      <img :src="ChartImg" alt="">
    </div>
  </even-columns>
</template>

<style scoped>

</style>