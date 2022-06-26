<template>
  <NavBar></NavBar>
  <CardsVue></CardsVue>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import CardsVue from "./components/CardsVue.vue";


export default {
  name: "App",
  components: {
    NavBar,CardsVue
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
.row{
  margin: 0px;
}
</style>
