<script setup lang="ts">

import Logo from "assets/images/icons/logo.svg";
import Facebook from "assets/images/icons/icon-facebook.svg";
import Youtube from "assets/images/icons/icon-youtube.svg";
import Twitter from "assets/images/icons/icon-twitter.svg";
import Pinterest from "assets/images/icons/icon-pinterest.svg";
import Instagram from "assets/images/icons/icon-instagram.svg";
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
            <logo style="width: 10rem" :fontControlled="false" filled/>
          </a>
          <ul class="social-media" role="list" aria-label="Social links">
            <li v-for="(link, index) in links" :key="index">
              <a :aria-label="link.label" :href="link.href">
                <component :is="link.icon"/>
              </a>
            </li>
          </ul>
        </div>
        <div class="footer-nav">
          <nav aria-label="Footer">
            <ul role="list">
              <li v-for="(item, index) in navItems" :key="index">
                <a class="text-neutral-100" :href="item.href">{{ item.title }}</a>
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
.social-media {
  display: flex;
  gap: var(--size-300);
}

a:hover, a:focus {
  color: var(--clr-accent-400);
}

.footer-nav {
  columns: 2;
}

a svg{
  font-size: var(--size-500);
}

@media (min-width: 50em) /* 800px */ {
  a svg{
    font-size: var(--size-400);
  }
}
</style>