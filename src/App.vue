<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
import LanguageSwitcher from '@/components/base/LanguageSwitcher.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <HelloWorld msg="Vue 3 Starter Kit" />
      <div class="nav-row">
        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/welcome">Welcome</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </nav>
        <div class="lang-switcher-wrap">
          <LanguageSwitcher />
        </div>
      </div>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.nav-row {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  margin-top: 2rem;
  flex-wrap: nowrap;
}

nav {
  font-size: 1.1em;
  text-align: center;
  display: flex;
  gap: 2rem;
  flex-wrap: nowrap;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
  white-space: nowrap;
}

nav a:first-of-type {
  border: 0;
}

.lang-switcher-wrap {
  flex-shrink: 0;
  display: flex;
  align-items: center;
}

@media (max-width: 700px) {
  .nav-row {
    flex-direction: column;
    align-items: stretch;
    gap: 1rem;
  }

  nav {
    justify-content: center;
    gap: 1.2rem;
  }

  .lang-switcher-wrap {
    justify-content: center;
    margin-top: 0.5rem;
  }
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .nav-row {
    margin-top: 1rem;
  }
}
</style>
