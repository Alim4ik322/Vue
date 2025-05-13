<script>
import Employee from './components/Employee.vue';
export default {
  name: 'App',
  components: {
   Employee
 }, 
 data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 }
      ]
    }
  }
}
</script>

<template>
  <div>
      <h2>Список работников</h2>
    <Employee
      v-for="user in users"
      :name="user.name"
      :salary="user.salary"
      :age="user.age"
      :key="user.id"
    />
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
