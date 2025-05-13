<script>
import CitySelection from './components/CitySelection.vue';
export default {
  name: 'App',
  components: {
     CitySelection

 }
}
</script>

<template>
  <div>
   <CitySelection />
  </div>
</template>

<style>
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
