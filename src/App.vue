<template>
  <div id="app">
    <div class="container">
      <Squares />
    </div>
  </div>
</template>

<script>
import Squares from "./components/Squares/Squares.vue";

export default {
  name: "App",
  components: {
    Squares,
  },
};
</script>

<style lang="scss">
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>
