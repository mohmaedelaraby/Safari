<template>
  <NavBar></NavBar>
  <banner-home></banner-home>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import BannerHome from "./components/BannerHome.vue";

export default {
  name: "App",
  components: {
    NavBar,
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
  color: #2c3e50;
}

.nav-link.dropdown-toggle::after {
  display: none;
}
* {
  margin: 0;
}
</style>
