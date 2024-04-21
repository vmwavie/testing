<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="logo-wrapper">
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" />
    </div>

    <div class="links-wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <div class="content-wrapper">
    <RouterView />
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  display: flex;
  align-items: center;
  background-color: var(--secondary-background-color);
  padding: var(--default-container-padding);
}

.logo-wrapper {
  flex: 0 0 auto; 
}

.logo {
  background-color: var(--secondary-background-color);
  display: block;
  width: 30px;
  height: 30px;
  padding-left: 5px;
  margin: 0;
}

.links-wrapper {
  margin-left: auto; 
}

nav {
  font-size: 12px;
}

nav a {
  background-color: var(--primary-button-background-color);
  color: var(--primary-button-text-color);
  border: 1px solid !important;
  border-color: var(--primary-button-border-desactived);
  padding: 5px 20px 5px 15px;
  border-radius: 3px;
}

nav a:first-child {
  margin-right: 5px;
}

nav a.router-link-exact-active, a:hover {
  border-color: var(--primary-button-border-active-color) !important;
  background-color: var(--primary-button-background-hover-color) !Important;
  color: var(--primary-button-text-hover-color);
}

nav a:first-of-type {
  border: 0;
}

.content-wrapper {
  padding: var(--default-container-padding);
}
</style>
