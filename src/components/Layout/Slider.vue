<template>
  <div>
    <q-carousel animated v-model="slide" arrows navigation infinite>
      <slot></slot>
    </q-carousel>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  setup() {
    return {
      slide: ref(1)
    }
  }
});
</script>

<style lang="scss">

</style>
