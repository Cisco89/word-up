<template>
  <div id="app">
    <ToDo></ToDo>
  </div>
</template>

<script>
import ToDo from './components/ToDo.vue'

export default {
  name: 'app',
  components: {
    ToDo
  },
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
.tittle {
    background: linear-gradient(-90deg, rgb(207, 106, 194), #16C0B0);
    padding: 15px;
    color: aliceblue;
    font-weight: 600;
}
</style>
