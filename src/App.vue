<template>
  <div id="app">
    <Eyes/>
    <Info/>
  </div>
</template>

<script>
import Eyes from './components/Animation.vue'
import Info from "./components/Info";

export default {
  name: 'App',
  components: {
    Eyes,
    Info
  }
}
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
