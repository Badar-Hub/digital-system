<template>
  <div class="row circle q-pa-md">
    <div class="col-xs-12 q-my-auto">
      <q-icon :name="data.img" size="sm" />
    </div>
    <div class="col-xs-12">
      <h6 class="q-my-sm">{{ data.heading }}</h6>
    </div>
    <div class="col-xs-12">
      <p>{{ data.paragraph }}</p>
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
.circle {
  width: 220px;
  height: 220px;
  border-radius: 50%;
  background-color: white;
  text-align: center;
  box-shadow: 0px 0px 8px 12px rgba(87, 152, 230, 1);
}
</style>
