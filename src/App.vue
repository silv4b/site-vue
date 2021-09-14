<template>
  <div id="app">
    <vue-scroll-progress-bar
      height="0.2rem"
      zIndex="999"
      backgroundColor="linear-gradient(to right, #fff, #fff)"
    />
    <div class="container">
      <Squares />
    </div>
  </div>
</template>

<script>
//TODO: Criar lógica pra alterar a variável 'backgroundColor' de acordo com o tema da página.

import Squares from "./components/Squares/Squares.vue";
import { VueScrollProgressBar } from "@guillaumebriday/vue-scroll-progress-bar";

export default {
  name: "App",
  components: {
    Squares,
    VueScrollProgressBar,
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
