<template>
  <div class="home">
    <hr class="q-my-none" />
    <div class="row header-image">
      <img src="@/assets/camera.jpeg" alt="camera" />
    </div>
    <div class="row justify-center items-center section pattern">
      <h4 class="q-my-lg">
        Get a Free Risk Assessment of your home by Our Security Expert
      </h4>
    </div>
    <div class="section">
      <div class="row justify-center heading">
        <h3 class="text-weight-medium q-my-lg">
          Solution We Offer
        </h3>
      </div>
      <div class="row width-lg">
        <div v-for="(card, index) in cards" :key="index" class="col-sm-4">
          <responsive-card class="q-ma-sm" :data="card" />
        </div>
      </div>
    </div>
    <div class="row justify-between section customer-support q-mt-lg">
      <div class="col col-xs-12 col-sm-5">
        <div class="support-image">
          <img
            src="@/assets/section/customer-support.jpeg"
            alt="customer-support"
          />
          <div class="absolute-center support-image-container q-pa-sm">
            <h4 class="q-my-sm">Reasons Why Should Choose Us?</h4>
          </div>
        </div>
      </div>
      <div class="col col-xs-12 col-sm-7 q-pa-xl">
        <div class="row q-ma-sm">
          <div
            v-for="(card, index) in choseCards"
            :key="index"
            class="col col-xs-6"
          >
            <chose-card class="q-ma-sm" :data="card" />
          </div>
        </div>
      </div>
    </div>
    <div class="section our-process q-mt-lg">
      <div class="row heading justify-center q-my-xl">
        <h3 class="cl-white q-my-sm">Our Process</h3>
      </div>
      <hr class="full-width" />
      <div class="row q-mt-md q-pb-xl">
        <div
          v-for="(circle, index) in processCircle"
          :key="index"
          class="row justify-center col-sm-4 q-my-md"
        >
          <process-circle class="q-ma-md" :data="circle" />
        </div>
        <div class="row full-width justify-center q-my-md">
          <h4 class="cl-white q-my-sm">
            Want to know more? It’s as easy.. Call Us on (00) 1234567890
          </h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import ChoseCard from '../components/Layout/ChoseCard.vue';
import ProcessCircle from '../components/Layout/ProcessCircle.vue';
import ResponsiveCard from '../components/Layout/ResponsiveCard.vue';

export default defineComponent({
  components: { ResponsiveCard, ChoseCard, ProcessCircle },
  setup() {
    const cards = ref([
      {
        img: 'https://cdn.quasar.dev/logo-v2/svg/logo.svg',
        heading: 'Heading Text',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        link: '/',
      },
      {
        img: 'https://cdn.quasar.dev/logo-v2/svg/logo.svg',
        heading: 'Heading Text',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        link: '/',
      },
      {
        img: 'https://cdn.quasar.dev/logo-v2/svg/logo.svg',
        heading: 'Heading Text',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        link: '/',
      },
      {
        img: 'https://cdn.quasar.dev/logo-v2/svg/logo.svg',
        heading: 'Heading Text',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        link: '/',
      },
      {
        img: 'https://cdn.quasar.dev/logo-v2/svg/logo.svg',
        heading: 'Heading Text',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        link: '/',
      },
    ]);
    const choseCards = ref([
      {
        img: 'schedule',
        heading: '24/7/365 Support',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'done',
        heading: 'Trustworthy',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'payments',
        heading: 'Affordable Rates',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'thumb_up',
        heading: 'Reliable and Proven',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'stacked_bar_chart',
        heading: 'Different Range',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'groups',
        heading: 'Experts and Staff',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
    ]);
    const processCircle = ref([
      {
        img: 'schedule',
        heading: '24/7/365 Support',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'done',
        heading: 'Trustworthy',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'payments',
        heading: 'Affordable Rates',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'thumb_up',
        heading: 'Reliable and Proven',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'stacked_bar_chart',
        heading: 'Different Range',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
      {
        img: 'groups',
        heading: 'Experts and Staff',
        paragraph:
          'Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus.',
        link: '/',
      },
    ]);

    return {
      cards,
      choseCards,
      processCircle,
    };
  },
});
</script>

<style lang="scss">
.home {
  .header-image {
    img {
      width: 100%;
      height: 500px;
      object-fit: cover;
    }
  }
  .pattern {
    height: 200px;
    color: white;
    background-color: #027f9a;
    background-image: url(../assets/section/pattern.png);
  }
  .customer-support {
    background-color: #fafafa;
    .support-image {
      position: relative;
      width: 43vw;
      height: 80vh;
      background-color: rgba(0, 0, 0, 0.425);
      overflow: hidden;
      @media (max-width: 599px) {
        width: 100vw;
        height: 60vh;
      }
      img {
        width: 43vw;
        height: 80vh;
        object-fit: cover;
        opacity: 0.6;
        overflow: hidden;
        @media (max-width: 599px) {
          width: 100vw;
          height: 60vh;
        }
      }
      .support-image-container {
        background-color: #027f9a;
        text-align: center;
        color: white;
        opacity: 0.8;
      }
    }
  }
  .our-process {
    background-color: #222222 !important;
    background-image: url(../assets/section/fw2.png);
  }
}
</style>
