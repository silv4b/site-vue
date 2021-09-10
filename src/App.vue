<template>
  <div id="app">
    <div class="container">
      <!-- <Toggle /> -->
      <Squares />
    </div>
  </div>
</template>

<script>
import Squares from "./components/Squares/Squares.vue";
//import Toggle from "./components/Toggle/Toggle.vue";

export default {
  name: "App",
  components: {
    Squares,
    //Toggle,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.container {
  z-index: 99 !important;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
