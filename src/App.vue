<template>
  <div id="app">
    <Squares />
  </div>
</template>

<script>
import Squares from "./components/Squares.vue";

export default {
  name: "App",
  components: {
    Squares,
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
