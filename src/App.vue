<script>
import EmployeeTable from './components/EmployeeTable.vue';

export default {
  name: 'App',
  components: {
   EmployeeTable
 }
}
</script>

<template>
  <div>
    <EmployeeTable/>
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
