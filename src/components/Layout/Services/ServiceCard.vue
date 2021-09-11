<template>
  <div class="service-card q-pa-md q-ma-md">
    <div class="row">
      <div class="col-xs-12">
        <h5 class="font-weight-bold q-my-sm">{{ data.heading }}</h5>
      </div>
      <div class="col-xs-12">
        <p class="text-body1 font-weight-bold q-mb-sm">{{ data.subheading }}</p>
      </div>
      <hr class="full-width" />
      <div class="price q-mt-md">
        <p class="text-body1 q-my-sm">Price</p>
        <div class="row full-width justify-center">
          <h3 class="q-my-sm">${{ data.price }}</h3>
          <h6 class="q-mt-auto q-mb-xs">/mo.</h6>
        </div>
      </div>
      <div
        v-for="(included, index) in data.included"
        :key="index"
        class="row full-width included"
      >
        <div class="col-xs-2 q-my-auto text-center">
          <q-icon size="lg" name="done" />
        </div>
        <div class="col-xs-10">
          <p class="text-body1 q-my-sm">
            {{ included }}
          </p>
        </div>
      </div>
      <div class="row full-width q-ma-md">
        <q-btn class="full-width" label="Customize Plan" color="secondary" />
      </div>
      <hr class="full-width bg-cl-aquamarine" />
      <div class="row full-width q-my-md">
        <q-btn color="primary" class="full-width" label="Learn More" />
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
.service-card {
  border-radius: 4px;
  box-shadow: rgb(0 0 0 / 10%) 0px 0px 16px 0px;
  background-color: rgb(255, 255, 255);
  border: 1px solid rgb(216, 216, 216);
}
</style>
