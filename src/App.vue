<template>
  <div id="app">
    <addBLog></addBLog>
  </div>
</template>

<script>
import addBLog from './components/addBLog.vue'

export default {
  name: 'app',
  components: {
    addBLog
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
