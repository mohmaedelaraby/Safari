<template>
  <swiper :navigation="true" :modules="modules" class="mySwiper">
    <template v-for="(item, index) in listofdata" v-bind:key="index">
      <swiper-slide>
        <TestMonelieCart :header="item.header" :txt="item.txt" />
      </swiper-slide>
    </template>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import TestMonelieCart from "./TestMonelieCart.vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";

// import required modules
import { Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
    TestMonelieCart,
  },

  data() {
    return {
      listofdata: [
        {
          header: "TESTIMONIALS",
          txt: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad ortis nisl ut aliquio consequat.",
        },
        {
          header: "TESTIMONIALS #2",
          txt: "Loremipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad ortis nisl ut aliquio consequat.",
        },
        {
          header: "TESTIMONIALS #3",
          txt: "Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad ortis nisl ut aliquio consequat.",
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

<style lang="css" scoped>
.swiper-button-next {
  right: 125px;
  left: auto;
  background-color: #8888;
  padding: 30px;
  border-radius: 10px;
  overflow: hidden;
}
.swiper-button-next::after {
  content: "next";
  font-size: 14px;
  color: white;
}

.swiper-button-prev {
  left: 125px;
  right: auto;
  background-color: #8888;
  padding: 30px;
  overflow: hidden;
  border-radius: 10px;
}
.swiper-button-prev::after {
  content: "prev";
  font-size: 14px;
  color: white;
}
</style>
