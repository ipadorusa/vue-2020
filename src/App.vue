<template>
  <div id="app">
    <Study01 />
    <Study02 />
  </div>
</template>

<script>
import Study01 from "./pages/Study01.vue";
import Study02 from "./pages/Study02.vue";

export default {
  name: "app",
  components: {
    Study01,
    Study02
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
