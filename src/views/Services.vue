<template>
  <div class="services">
    <div class="row">
      <div v-for="(data, index) in packages" :key="index" class="col-xs-4">
        <service-card :data="data" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import ServiceCard from '@/components/Layout/Services/ServiceCard.vue';
import { defineComponent } from '@vue/runtime-core';
import { ref } from 'vue';
export default defineComponent({
  components: { ServiceCard },
  setup() {
    const packages = ref([
      {
        heading: 'For basic protection',
        subheading: 'Smart Camera',
        price: '12',
        included: [
          'Control from your smartphone with the SmartHome app',
          'Choice of one Indoor, Outdoor or Doorbell Camera',
        ],
      },
      {
        heading: 'For a smarter home',
        subheading: 'Smart Automation Plus',
        price: '15',
        included: [
          'Control from your smartphone with the SmartHome app',
          'Choice of 2 automation devices',
          'Choice of 1 security camera',
        ],
      },
      {
        heading: 'For advanced protection',
        subheading: 'Secure',
        price: '27',
        included: [
          '1 Control Panel',
          '2 Door/Window Sensors',
          '1 Motion Sensor',
        ],
      },
      {
        heading: 'For total protection',
        subheading: 'Control + Video',
        price: '40',
        included: [
          '1 Control Panel',
          '2 Door/Window Sensors',
          '1 Motion Sensor',
          'Choice of 3 security or automation devices',
          'Choice of 1 security camera',
        ],
      },
    ]);

    return {
      packages,
    };
  },
});
</script>

<style lang="scss"></style>
