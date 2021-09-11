<template>
  <div class="row chose-card">
    <div class="col-xs-4 text-center">
      <q-icon class="q-my-md q-pa-sm" :name="data.img" size="md" />
    </div>
    <div class="col-xs-8">
      <h6 class="q-my-sm text-weight-bold">{{ data.heading }}</h6>
      <p class="text-body1 q-my-sm">
        {{ data.paragraph }}
      </p>
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
.chose-card {
  img {
    max-width: 70px;
  }
  i {
    color: #027f9a;
    border: 1px solid black;
  }
  &:hover {
    i {
      transition: 0.5s;
      border: unset;
      background-color: #027f9a;
      color: white;
    }
  }
}
</style>
