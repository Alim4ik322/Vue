<script>
import InputToggle1 from './components/InputToggle1.vue';
import InputToggle2 from './components/InputToggle2.vue';

export default {
  name: 'App',
  components: {
    InputToggle1,
    InputToggle2
 }
}
</script>

<template>
  <div>
  <InputToggle1 />
  <InputToggle2 />

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
