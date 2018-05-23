<template>
  <div id="app">
    <ObliqueStrategies/>
  </div>
</template>

<script>
import ObliqueStrategies from './components/ObliqueStrategies'

export default {
  name: 'App',
  components: {
    ObliqueStrategies
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
