<template>
  <div class="footer">
    <div class="row justify-center heading q-pt-xl">
      <h3 class="cl-white q-my-sm">Tell Your Security Needs</h3>
    </div>
    <div class="row width-lg q-my-md">
      <h4 class="cl-white q-my-sm">Interested In:</h4>
    </div>
    <div class="row width-lg">
      <div
        v-for="(value, index) in values"
        :key="index"
        class="col col-xs-6 col-sm-4 q-px-xl q-py-sm"
      >
        <q-radio
          class="cl-white q-my-sm"
          dense
          v-model="shape"
          :val="value"
          :label="value"
        />
      </div>
    </div>
    <div class="row justify-center width-lg q-my-md">
      <q-btn class="q-pa-sm" label="Click Here To Submit" color="primary" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    const values = ref([
      'Video Verification',
      'Access Control Systems',
      'Alarm Systems',
      'Door Controls',
      'Retail Video Analytics',
      'Smart Phone Security',
      'IP Video',
      'Record Movements',
      '24 Hour Monitoring',
      'Cloud Monitoring',
    ]);
    const selectedValues = ref([]);

    return {
      selectedValues,
      values,
    };
  },
});
</script>

<style lang="scss">
.footer {
  height: 500px;
  background-size: cover;
  background-color: #027f9a;
  background-image: url(../../assets/section/fw2.png);
  .q-radio__bg {
    color: white;
  }
}
</style>
