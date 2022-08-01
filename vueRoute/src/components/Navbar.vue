<script>
import { RouterLink, RouterView } from "vue-router";

export default {
  data: function () {
    return {
      ids: [1, 2, 3, 4, 5, 6],
    };
  },
  methods: {},
};
</script>

<template>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
    <RouterLink to="/contact">Contact</RouterLink>
    <RouterLink
      v-for="(id, i) in ids"
      :to="{ name: 'profile', params: { id: id } }"
      :key="i"
      >profile {{ id }}</RouterLink
    >
  </nav>
  <RouterView />
</template>

<style scoped>
nav {
  width: 100%;
  font-size: 20px;
  text-align: center;
  margin-top: 2rem;
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
}

nav a:first-of-type {
  border: 0;
}
</style>
