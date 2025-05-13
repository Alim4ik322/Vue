<script>
import LanguageSelection from './components/LanguageSelection.vue';
export default {
  name: 'App',
  components: {
     LanguageSelection

 }
}
</script>

<template>
  <div>
   <LanguageSelection />

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
