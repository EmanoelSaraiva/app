<template>
  <!-- Usar o component no template -->
  <TheHeader />
  <Home />
</template>

<script>
import TheHeader from "./components/TheHeader";
import Home from "./components/HelloWorld";
//Primeiro deve ser importado

//Declara o component
export default {
  name: "App",
  components: {
    TheHeader,
    Home,
  },
  data() {
    return {
      showName: false,
    };
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
  margin-top: 60px;
}
</style>
./components/TheHeader.vue
