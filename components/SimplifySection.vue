<script setup lang="ts">

import EvenColumns from "~/components/UI/containers/EvenColumns.vue";
import AButton from "~/components/UI/AButton.vue";
</script>

<template>
  <even-columns class="cta | bg-accent-400 text-neutral-100 padding-block-700">
    <div>
      <p class="fs-primary-heading fw-bold">
        Simplify how your team works today.
      </p>
    </div>
    <div class="simplify-button">
      <a-button inverted/>
    </div>
  </even-columns>
</template>

<style scoped>
.cta {
  position: relative;
  isolation: isolate;
  text-align: unset;
}

.cta:before {
  content: '';
  position: absolute;
  inset: 0;
  z-index: -1;
  background-image: url("assets/images/bg-tablet-pattern.svg"), url("assets/images/bg-tablet-pattern.svg");
  background-repeat: no-repeat;
  background-position: -15rem -5rem, 80rem -42rem;
  opacity: 0.1;
}

@media (max-width: 50em) {
  .cta{
    text-align: center;
  }

  .cta:before {

  }
}

.simplify-button {
  margin: auto 0 auto auto;
}

@media (max-width: 50em) {
  .simplify-button {
    margin: auto;
  }
}
</style>