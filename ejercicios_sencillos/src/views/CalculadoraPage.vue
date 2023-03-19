<template>
  <CalculadoraComponent msg="Ejercicios Sencillos en Vue.js" />
</template>

<script>
import CalculadoraComponent from "../components/CalculadoraComponent.vue"

export default {
  name: "App",
  components: {
    CalculadoraComponent,
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
  
  /* margin-top: 60px; */
}
</style>