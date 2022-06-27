<template>
  <swiper :navigation="true" :modules="modules" class="mySwiper">
    <swiper-slide v-for="(item, index) in listofdata" v-bind:key="index">
      <BannerCart :txt="item.txt" />
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";

// import required modules
import { Navigation } from "swiper";
import BannerCart from "./BannerCart.vue";

export default {
  components: {
    Swiper,
    SwiperSlide,
    BannerCart
},

  data() {
    return {
      listofdata: [
        {
          txt: "Forst #1",
        },
        {
          txt: "Forst #2",
        },
        {
          txt: "Forst #3",
        },
      ],
    };
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>
