<script setup lang="ts">

import Logo from "assets/images/logo.svg";
import Facebook from "assets/images/icon-facebook.svg";
import Youtube from "assets/images/icon-youtube.svg";
import Twitter from "assets/images/icon-twitter.svg";
import Pinterest from "assets/images/icon-pinterest.svg";
import Instagram from "assets/images/icon-instagram.svg";
import AButton from "~/components/UI/AButton.vue";

const links = [
  {
    label: 'Facebook',
    icon: Facebook,
    href: '#',
  },
  {
    label: 'Youtube',
    icon: Youtube,
    href: '#',
  },
  {
    label: 'Twitter',
    icon: Twitter,
    href: '#',
  },
  {
    label: 'Pinterest',
    icon: Pinterest,
    href: '#',
  },
  {
    label: 'Instagram',
    icon: Instagram,
    href: '#',
  },
]

const navItems = [
  {
    title: 'Home',
    href: '#',
  },
  {
    title: 'Pricing',
    href: '#',
  },
  {
    title: 'Products',
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
  {
    title: 'Privacy Policy',
    href: '#',
  },
]

</script>

<template>
  <footer class="bg-neutral-900 text-neutral-100 padding-block-700">
    <div class="container">
      <div class="even-columns">
        <div>
          <a href="#">
            <img :src="Logo" alt="Manage">
          </a>
          <ul role="list" aria-label="Social links">
            <li v-for="(link, index) in links" :key="index">
              <a :aria-label="link.label" :href="link.href">{{link.icon}}</a>
            </li>
          </ul>
        </div>
        <div>
          <nav aria-label="Footer">
            <ul role="list">
              <li v-for="(item, index) in navItems" :key="index">
                <a :href="item.href">{{ item.title }}</a>
              </li>
            </ul>
          </nav>
        </div>
        <div>
          <form action="">
            <input type="email">
            <a-button text="Go"/>
            <p>Copyright 2024. All rights Reserved</p>
          </form>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>

</style>