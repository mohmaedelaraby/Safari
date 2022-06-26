<template>
  <swiper :navigation="true" :modules="modules" class="mySwiper" >
    <swiper-slide v-for="item in 4" v-bind:key="item"> <TestMonelieCart /> </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import TestMonelieCart from './TestMonelieCart.vue'

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";



// import required modules
import { Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,TestMonelieCart
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>
