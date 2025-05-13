<script>
import Employee from './components/Employee.vue';

export default {
  components: {
    Employee
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
    updateEmployee(id, name, salary, age) {
      this.employees = this.employees.map(employee => {
        if (employee.id === id) {
          employee.name = name;
          employee.salary = salary;
          employee.age = age;
        }
        return employee;
      });
    }
  }
}
</script>
<template>
  <div>
    <h2>Список сотрудников</h2>
    <Employee
      v-for="employee in employees"
      :key="employee.id"
      :id="employee.id"
      :name="employee.name"
      :salary="employee.salary"
      :age="employee.age"
      @remove="removeEmployee"
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
