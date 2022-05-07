<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <main>
    <header>
      <img
        alt="Vue logo"
        class="logo"
        src="./assets/logo.svg"
        width="125"
        height="125"
      />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </header>
    <RouterView />
  </main>
</template>

<style>
@import "./assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

header {
  line-height: 1.5;
  max-height: 100vh;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  text-decoration: none;
  color: gray;

  transition: 0.4s;
}

nav a.router-link-exact-active {
  color: hsla(160, 100%, 37%, 1);
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}
</style>
