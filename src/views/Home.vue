<template>
  <div class="home">
    <hr class="q-my-none" />
    <div class="row header-image relative">
      <div
        class="row top60 full-width justify-between q-ma-md q-pa-md absolute"
      >
        <q-icon
          class="q-my-sm cursor-pointer"
          color="primary"
          size="lg"
          name="arrow_back_ios"
          @click="previousSlide"
        />
        <q-icon
          class="q-my-sm cursor-pointer"
          color="primary"
          size="lg"
          name="arrow_forward_ios"
          @click="nextSlide"
        />
      </div>
      <img
        v-for="(image, index) in slides"
        :key="index"
        v-show="index === selectedIndex"
        class="slide-image fade"
        :src="require(`@/assets/section/${image}`)"
        :alt="image"
      />
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
    <security-needs />
    <div class="row width-lg q-my-md our-clients">
      <div class="col-sm-6 text-center our-client q-pa-md q-py-xl">
        <h4 class="cl-white q-my-lg">Hear from Our Clients</h4>
        <p class="cl-white text-body1 q-my-xl">
          “ Etiam ultricies nisi vel augue. Curabitur ullamcorper ultricies
          nisi. Nam eget dui. Etiam rhoncus. “
        </p>
        <h6 class="cl-white q-my-lg">Steve Austin - Managing Director</h6>
      </div>
      <div class="col-sm-3 q-pa-md q-my-auto">
        <div class="client-container text-center">
          <img class="client-img" src="@/assets/section/client.jpeg" />
          <p class="text-body1 q-my-sm">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
          </p>
        </div>
      </div>
      <div class="col-sm-3 q-pa-md q-my-auto">
        <div class="client-container text-center">
          <img class="client-img" src="@/assets/section/client.jpeg" />
          <p class="text-body1 q-my-sm">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
          </p>
        </div>
      </div>
    </div>
    <div class="ideas">
      <div class="row width-lg q-pa-xl">
        <h4 class="q-mt-lg q-mb-none">Have any ideas in your mind?</h4>
        <div class="row full-width justify-between">
          <h2 class="q-my-sm cl-white">We provide leading security systems</h2>
          <q-btn class="q-my-sm" label="Request A Quote" color="black" />
        </div>
      </div>
    </div>
    <div class="compaines width-lg">
      <div class="row heading justify-center">
        <h3 class="q-my-xl font-weight-bolder">
          Companies We Have as Clients
        </h3>
      </div>
      <div class="row">
        <div class="col col-sm-3 text-center">
          <img class="images" src="@/assets/section/logo/01.png" />
        </div>
        <div class="col col-sm-3 text-center">
          <img class="images" src="@/assets/section/logo/01.png" />
        </div>
        <div class="col col-sm-3 text-center">
          <img class="images" src="@/assets/section/logo/01.png" />
        </div>
        <div class="col col-sm-3 text-center">
          <img class="images" src="@/assets/section/logo/01.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import SecurityNeeds from '@/components/Layout/SecurityNeeds.vue';
import { defineComponent, onMounted, ref } from 'vue';
import ChoseCard from '../components/Layout/ChoseCard.vue';
import ProcessCircle from '../components/Layout/ProcessCircle.vue';
import ResponsiveCard from '../components/Layout/ResponsiveCard.vue';

export default defineComponent({
  components: { ResponsiveCard, ChoseCard, ProcessCircle, SecurityNeeds },
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
        heading: 'Technical Suport',
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
    const slides = ref(['hikvision.png', 'clover-slide.png', 'hikvision.png', 'clover-slide.png']);
    const selectedIndex = ref(0);
    const nextSlide = () => {
      if (selectedIndex.value === slides.value.length - 1) {
        selectedIndex.value = 0;
      } else {
        selectedIndex.value++;
      }
    };
    const previousSlide = () => {
      if (selectedIndex.value === 0) {
        selectedIndex.value = slides.value.length - 1;
      } else {
        selectedIndex.value--;
      }
    };

    onMounted(() => {
      setInterval(() => {
        if(selectedIndex.value === slides.value.length -1) {
          selectedIndex.value = 0
        } else {
          selectedIndex.value++
        }
      }, 5000)
    })
    return {
      cards,
      slides,
      choseCards,
      nextSlide,
      previousSlide,
      processCircle,
      selectedIndex,
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
  .our-clients {
    .our-client {
      background-color: rgb(37, 37, 37);
    }
    .client-container {
      max-width: 250px;
      width: 100%;
      .client-img {
        max-width: 250px;
        width: 100%;
        object-fit: cover;
      }
    }
  }
  .ideas {
    background-image: url(../assets/section/pattern.png);
    background-color: #027f9a;
  }
  .companies {
    .images {
      max-width: 250px;
      width: 100%;
    }
  }
  .slide-image {
    transition: 0.6s ease;
  }
  /* Fading animation */
  .fade {
    -webkit-animation-name: fade;
    -webkit-animation-duration: 1.5s;
    animation-name: fade;
    animation-duration: 1.5s;
  }

  @-webkit-keyframes fade {
    from {
      opacity: 0.4;
    }
    to {
      opacity: 1;
    }
  }

  @keyframes fade {
    from {
      opacity: 0.4;
    }
    to {
      opacity: 1;
    }
  }

  /* On smaller screens, decrease text size */
  @media only screen and (max-width: 300px) {
    .prev,
    .next,
    .text {
      font-size: 11px;
    }
  }
}
</style>
