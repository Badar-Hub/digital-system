<template>
  <div class="row header-top q-pa-sm justify-center">
    <q-icon name="error" class="cl-red q-my-xs" size="md" />
    <p class="text-body2 cl-red q-ma-sm">
      COVID-19:
    </p>
    <p class="text-body2 cl-white q-my-sm">
      Learn how we’re supporting communities and helping Canadians stay
      connected.
    </p>
  </div>
  <div class="header">
    <div class="row top-bar"></div>
    <div class="row justify-between q-px-xl">
      <router-link to="/">
        <img class="logo" src="@/assets/logo.jpeg" alt="web-logo" />
      </router-link>
      <nav class="q-my-auto">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/services">Services</router-link>
        <router-link to="/">Shop</router-link>
        <router-link to="/">Contact</router-link>
      </nav>
    </div>
  </div>
  <hr class="full-width q-my-none" />
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({});
</script>

<style lang="scss">
.header-top {
  background-color: black;
}
.router-link-active {
  color: #00cbf8 !important;
}
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
