<script setup lang="ts">
import Logo from '~/assets/images/logo.svg'
import MenuOpen from '~/assets/images/icon-close.svg'
import MenuClose from '~/assets/images/icon-hamburger.svg'
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

const toggleMenu = ref(false)

let toggle = () => {
  toggleMenu.value = !toggleMenu.value
}

</script>

<template>
  <div class="overlay" :data-overlay="toggleMenu">
  </div>
  <header class="header">
    <div class="container">
      <div class="nav-wrapper">
        <a href="#">
          <img :src="Logo" alt="Manage">
        </a>
        <button @click="toggle" class="mobile-nav-toggle" aria-controls="primary-navigation"
                :aria-expanded="toggleMenu">
          <img :src="toggleMenu ? MenuOpen : MenuClose" alt="" aria-hidden="true">
          <span class="visually-hidden">Menu</span>
        </button>
        <nav aria-label="Primary"
             :data-visible="toggleMenu"
             class="primary-navigation"
             id="primary-navigation">
          <ul class="nav-list" role="list">
            <li v-for="(item, index) in navItems" :key="index">
              <a :href="item.href">{{ item.title }}</a>
            </li>
          </ul>
        </nav>
        <a-button class="nav-button"/>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  top: var(--size-700);
  position: sticky;
  margin-bottom: var(--size-700);
}

.nav-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.mobile-nav-toggle {
  display: none;
}

.nav-list {
  display: flex;
  gap: clamp(var(--size-400), 5vw, var(--size-600));
  font-size: var(--fs-nav);
  font-weight: var(--fw-semi-bold);
}

@media (max-width: 50em) {
  .primary-navigation {
    display: none;

    position: fixed;
    padding: var(--size-700);
    inset: 7rem var(--size-400) auto;
    background: var(--clr-neutral-100);
    border-radius: var(--size-100);
    box-shadow: 0 0 0.75em rgba(0, 0, 0, 0.05);
  }

  .overlay[data-overlay=true] {
    position: fixed;
    inset: 0;
    background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));
  }

  .primary-navigation[data-visible=true] {
    display: block;
  }

  .nav-list {
    display: grid;
    gap: var(--size-600);
    text-align: center;
    font-weight: var(--fw-bold);
  }

  .nav-list a:hover,
  .nav-list a:focus {
    color: var(--clr-accent-400);
  }

  .mobile-nav-toggle {
    display: block;
    width: 40px;
    height: 40px;
    cursor: pointer;
    background: transparent;
    border: 0;
    padding: 0.5em;
  }

  .nav-button {
    display: none;
  }
}
</style>