<script>
import DynamicStyles from './components/DynamicStyles.vue';
export default {
  name: 'App',
  components: {
     DynamicStyles
 }
}
</script>

<template>
  <div>
        <h1>Пример динамических классов</h1>
    <DynamicStyles />
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
