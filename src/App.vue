<template>
  <div id="app">
    <Blocos/>
    <Squares/>
  </div>
</template>

<script>
//import Blocos from './components/Blocos.vue'
import Squares from './components/Squares.vue'

export default {
  name: 'App',
  components: {
    //Blocos,
    Squares
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
