<template>
  <div class="responsive-card q-pa-sm">
    <div class="row">
      <div class="col-xs-4 text-center q-my-auto">
        <img :src="data.img" :alt="data.img" />
      </div>
      <div class="col-xs-8">
        <h6 class="q-my-sm">{{ data.heading }}</h6>
        <p class="text-body1 overflow-hidden-y	">
          {{ data.paragraph }}
        </p>
        <router-link to="/">Read More ></router-link>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    data: {
      type: Object,
    },
  },
});
</script>

<style lang="scss">
.responsive-card {
  img {
    max-width: 70px;
    width: 100%;
  }
  p {
    height: 95px;
    overflow: hidden;
  }
  a {
    color: black;
    font-size: 18px;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
  border: 1px solid rgba(138, 135, 135, 0.356);
  &:hover {
    background-color: #047a94;
    color: white;
    transition: 0.5s;
    a {
      color: white;
      transition: 0.5s;
    }
  }
}
</style>
