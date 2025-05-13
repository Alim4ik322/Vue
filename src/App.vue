<script>
import Employee from './components/Employee.vue';
export default {
  name: 'App',
  components: {
   Employee
 }
}
</script>

<template>
  <div>
    <h2>Главный компонент</h2>
    <Employee name="Михаил"e="Иванов" age="30" />
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
