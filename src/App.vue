<template>
  <NavBar></NavBar>
  <CardsVue></CardsVue>
  <FilterSection/>
  <FooterSection/>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import CardsVue from "./components/CardsVue.vue";
import FilterSection from "./components/Filteretion/FilterSection.vue";
import FooterSection from "./components/FooterSection.vue";


export default {
  name: "App",
  components: {
    NavBar,
    CardsVue,
    FilterSection,
    FooterSection
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
.row{
  margin: 0px;
}
</style>
