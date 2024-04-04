<template>
  <!-- Usar o component no template -->
  <TheHeader />
  <Home />
  <br />
  <Computed_Todo />
</template>

<script>
import TheHeader from "./components/TheHeader";
import Home from "./components/HelloWorld";
import Computed_Todo from "./components/Computeds";
//Primeiro deve ser importado

//Declara o component
export default {
  name: "App",
  components: {
    TheHeader,
    Home,
    Computed_Todo,
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
  color: #2c3e50;
  margin-top: 60px;
}
</style>
./components/TheHeader.vue
