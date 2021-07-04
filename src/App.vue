<template>
  <div id="app">
    <Template />
  </div>
</template>

<script>
//import Squares from "./components/Squares.vue";
import Template from "./components/Template.vue";

export default {
  name: "App",
  components: {
    //Squares,
    Template,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
