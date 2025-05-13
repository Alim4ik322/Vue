<script>
import Employee from './components/Employee.vue';
export default {
  name: 'App',
  components: {
   Employee
 }, 
  methods: {
    func(name) {
      console.log('Полученное имя:', name);
    }
  }
}
</script>

<template>
  <div>
     <h2>Главный компонент</h2>
    <Employee name="Алим" @sendName="func" />
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
