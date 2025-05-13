<script>
export default {
  props: {
    name: String,
    salary: Number,
    age: Number
  }
}
</script>

<template>
  <div class="employee-card">
    <p><strong>Имя:</strong> {{ name }}</p>
    <p><strong>Зарплата:</strong> {{ salary }}</p>
    <p><strong>Возраст:</strong> {{ age }}</p>
  </div>
</template>

<style scoped>
.employee-card {
  border: 1px solid #ddd;
  padding: 10px;
  margin: 10px 0;
  border-radius: 5px;
  background-color: #f9f9f9;
}
</style>
