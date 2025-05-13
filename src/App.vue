<script>
import Employee from './components/Employee.vue';
import EmployeeForm from './components/EmployeeForm.vue';

export default {
  components: {
    Employee,
    EmployeeForm
  },
  data() {
    return {
      employees: [
        { id: 1, name: 'Алим', salary: 1000, age: 30 },
        { id: 2, name: 'Иван', salary: 2000, age: 40 },
        { id: 3, name: 'Мария', salary: 3000, age: 50 }
      ]
    }
  },
  methods: {
    addEmployee(name, salary, age) {
      let id = this.employees.length + 1;
      this.employees.push({ id, name, salary, age });
    }
  }
}
</script>

<template>
  <div>
    <h2>Список сотрудников</h2>
    <EmployeeForm @add="addEmployee" />
    <Employee
      v-for="employee in employees"
      :key="employee.id"
      :id="employee.id"
      :name="employee.name"
      :salary="employee.salary"
      :age="employee.age"
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
