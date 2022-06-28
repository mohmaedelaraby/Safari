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
@import '@/assets/styles/main.css'
</style>
