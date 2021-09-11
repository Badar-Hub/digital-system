<template>
  <header-sp />
  <router-view></router-view>
  <footer-sp />
</template>

<script lang="ts">
import { defineComponent } from '@vue/runtime-core';
import HeaderSp from './components/Layout/Header.vue';
import FooterSp from './components/Layout/Footer.vue';

export default defineComponent({
  components: {
    HeaderSp,
    FooterSp,
  },
});
</script>

<style lang="scss">
.width-lg {
  max-width: 1200px;
  margin: auto;
}
.cl-white {
  color: white;
}
.cl-black {
  color: black;
}
</style>
