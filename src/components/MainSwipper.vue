<template>
  <swiper
    :modules="modules"
    :navigation="true">
    <swiper-slide v-for="(item, index) in items" :key="index">
      <slot name="cards" :header="item.header" :txt="item.txt"></slot>
    </swiper-slide>
  </swiper>
</template>
<!-- Start Script -->
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper";
import "swiper/css";
import "swiper/css/navigation";
export default {
  props: [
    "items",
  ],
  components: { Swiper, SwiperSlide },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>