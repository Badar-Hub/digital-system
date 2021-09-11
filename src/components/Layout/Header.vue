<template>
  <div class="header">
    <div class="row top-bar"></div>
    <div class="row justify-between q-px-xl">
      <img class="logo" src="@/assets/logo.jpeg" alt="web-logo" />
      <nav class="q-my-auto">
        <router-link to="/">Home</router-link>
        <router-link to="/">About</router-link>
        <router-link to="/">Packages</router-link>
        <router-link to="/">Security System</router-link>
        <router-link to="/">Services</router-link>
        <router-link to="/">Shop</router-link>
        <router-link to="/">Contact</router-link>
      </nav>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({});
</script>

<style lang="scss">
.header {
  nav {
    a {
      padding-left: 20px;
      text-decoration: none;
      color: black;
      font-size: 20px;
      &:hover {
        text-decoration: underline;
      }
    }
  }
  .logo {
    max-width: 200px;
    width: 100%;
  }
}
</style>
