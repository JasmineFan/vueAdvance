<template>
  <div id="app">
    <advanced-use/>
  </div>
</template>

<script>
import AdvancedUse from './components/AdvancedUse'

export default {
  name: 'app',
  components: {
    AdvancedUse
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
