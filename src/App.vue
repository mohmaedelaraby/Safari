<template>
  <NavBar></NavBar>
  <BannerHome/>
  <CardsVue></CardsVue>
  <FilterSection />
  <TestMoneliesSwipper />
  <FooterSection />
</template>

<script>
import NavBar from "./components/NavBar.vue";
import CardsVue from "./components/CardsVue.vue";
import FilterSection from "./components/Filteretion/FilterSection.vue";
import FooterSection from "./components/FooterSection.vue";

import TestMoneliesSwipper from "./components/TestMoneliesSwipper.vue";
import BannerHome from "./components/BannerHome.vue";

export default {
  name: "App",
  components: {
    NavBar,
    CardsVue,
    FilterSection,
    FooterSection,
    TestMoneliesSwipper,
    BannerHome
},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.nav-link.dropdown-toggle::after {
  display: none;
}
* {
  margin: 0;
  overflow-x: hidden;
}
.row {
  margin: 0px;
}
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
