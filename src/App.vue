<template>
  <!-- Usar o component no template -->
  <TheHeader />
  <ObserverS />
  <!-- <Home />
  <br />
  <Computed_Todo /> -->
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import ObserverS from "./components/ObserverS.vue";
// import Home from "./components/HelloWorld";
// import Computed_Todo from "./components/Computed_Todo";
//Primeiro deve ser importado

//Declara o component
export default {
  name: "App",
  components: {
    TheHeader,
    ObserverS,
    // Home,
    // Computed_Todo,
  },
  data() {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #cdd8e4;
  background-color: #2c3e50;
}
</style>
./components/TheHeader.vue
