<script setup lang="ts">
import EvenColumns from "~/components/UI/containers/EvenColumns.vue";

const listItems = [
  {
    title: 'Track company-wide progress',
    text: 'See how your day-to-day tasks fit into the wider vision.\n' +
        'Go from tracking progress at the milestone level all the\n' +
        'way done to the smallest of details. Never lose sight of\n' +
        'the bigger picture again.',
  },
  {
    title: 'Advanced built-in reports',
    text: 'Set internal delivery estimates and track progress toward\n' +
        'company goals. Our customizable dashboard helps you\n' +
        'build out the reports you need to keep key stakeholders\n' +
        'informed.',
  },
  {
    title: 'Everything you need in one place',
    text: 'Stop jumping from one service to another to\n' +
        'communicate, store files, track tasks and share\n' +
        'documents. Manager offers an all-in-one team\n' +
        'productivity solution.',
  },
]
</script>

<template>
  <even-columns class="padding-block-900">
    <div>
      <h2 class="fs-secondary-heading fw-bold">
        What's different about Manage?
      </h2>
      <p>Manager provides all the functionality your
        team needs, without the complexity. Our
        software is tailor-made for modern digital
        product teams.</p>
    </div>
    <div>
      <ul role="list">
        <li v-for="(item, index) in listItems" :key="index">
          <h3 class="fs-600 fw-bold">{{ item.title }}</h3>
          <p>{{ item.text }}</p>
        </li>
      </ul>
    </div>
  </even-columns>
</template>

<style scoped>

</style>