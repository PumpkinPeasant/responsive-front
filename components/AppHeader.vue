<script setup lang="ts">
import Logo from '~/assets/images/logo.svg'
import AButton from "~/components/UI/AButton.vue";

const navItems = [
  {
    title: 'Pricing',
    href: '#',
  },
  {
    title: 'Product',
    href: '#',
  },
  {
    title: 'About Us',
    href: '#',
  },
  {
    title: 'Careers',
    href: '#',
  },
  {
    title: 'Community',
    href: '#',
  },
]

</script>

<template>
  <header>
    <div class="container">
      <a href="#">
        <img :src="Logo" alt="Manage">
      </a>
      <nav aria-label="Primary">
        <ul role="list">
          <li v-for="(item, index) in navItems" :key="index">
            <a :href="item.href">{{ item.title }}</a>
          </li>
        </ul>
      </nav>
      <a-button/>
    </div>
  </header>
</template>

<style scoped>

</style>