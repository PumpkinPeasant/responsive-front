<script setup lang="ts">
const props = defineProps({
  inverted: {type: Boolean, required: false, default: false},
  text: {type: String, required: false, default: 'Get Started'},
});
</script>

<template>
  <button
      :class="inverted ? 'white' : 'orange'"
      class="button">{{ text }}
  </button>
</template>

<style scoped>
.button {
  border: 0;
  border-radius: 100vmax;
  padding: 1.25em 2.5em;
  line-height: 1;
  font-weight: var(--fw-bold);
  font-size: var(--fs-button);
  box-shadow: 0 1.125em 1em -1em var(--clr-accent-500);
}

.orange {
  color: var(--clr-neutral-100);
  background: var(--clr-accent-400);
}

.orange:hover,
.orange:focus-visible {
  background: var(--clr-accent-300);
}

.white {
  color: var(--clr-accent-400);
  background: var(--clr-neutral-100);
}

.white:hover,
.white:focus-visible {
  color: var(--clr-accent-300);
}

</style>