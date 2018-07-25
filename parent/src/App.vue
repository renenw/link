<template>
  <div id="app">
    <p>Parent</p>
    Child: [<Child />]
  </div>
</template>

<script>
import Child from 'child'

export default {
  name: 'App',
  components: {
    Child
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
