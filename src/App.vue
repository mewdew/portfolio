<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <nav :class="{ animated: $route.path === '/' }">
    <div class="logoContainer">
      <RouterLink to="/">
        <img
          alt="App logo"
          class="logo"
          :class="{ rotating: $route.path === '/' }"
          src="./assets/logo-s.svg"
        />
      </RouterLink>
    </div>
    <div class="navLinks">
      <RouterLink to="/work">Work</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </div>
  </nav>
  <RouterView />
</template>

<style scoped>
@keyframes rotating {
  from {
    transform: scale(1) rotate(0deg);
  }
  to {
    transform: scale(6) rotate(360deg);
  }
}

.rotating {
  animation: rotating 6s ease-in infinite;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}
nav.animated {
  height: 100vh;
  width: 100vw;
  flex-direction: column;
}
.logo {
  display: block;
  position: relative;
  width: 45px;
  height: 45px;
}

nav.animated .logo {
  position: fixed;
  top: 50%;
  left: 50%;
}

nav.animated .navLinks {
  position: absolute;
  bottom: 20%;
  font-size: 1.5rem;
}
nav .navLinks {
  font-size: 1rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  display: flex;
  justify-content: space-between;
  padding: 0.5rem;
  background: black;
  align-items: center;
}

nav a.router-link-exact-active {
  color: rgb(245, 245, 245);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  main {
    height: calc(100vh - 67px);
    overflow: auto;
  }
}
</style>
