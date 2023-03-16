<template>
  <div
    class="d-flex flex-column flex-md-row align-items-center py-3 mb-4 border-bottom"
  >
    <a class="d-flex align-items-center text-dark text-decoration-none" >
      <img :src="logo" alt="logo"  style="width: 250px; cursor: pointer;" @click="toHomeHandler" />
    </a>
    <nav class="d-inline-flex mt-2 mt-md-0 ms-md-auto">
      <a >
        <router-link :to="{ name: 'login' }" class="me-3 py-2 text-dark text-decoration-none">Login</router-link>
      </a>
      <a >
        <router-link :to="{ name: 'register' }" class="me-3 py-2 text-dark text-decoration-none">Register</router-link>
      </a>
    </nav>
  </div>
</template>

<script>
import { logo } from "../constants/index";
export default {
  data() {
    return {
      logo,
    };
  },
  methods: {
    toHomeHandler() {
      return this.$router.push("/");
    },
  },
};
</script>

<style>
</style>