<script>
export default {
  props: {
    name: String,      // Имя сотрудника
    surname: String,   // Фамилия сотрудника
    age: Number,       // Возраст сотрудника
    salary: Number,    // Зарплата сотрудника
    isActive: Boolean  // Активный статус сотрудника
  }
}
</script>

<template>
  <div>
    <h3>Информация о сотруднике</h3>
    <p>Имя: {{ name }}</p>
    <p>Фамилия: {{ surname }}</p>
    <p>Возраст: {{ age }}</p>
    <p>Зарплата: {{ salary }}</p>
    <p>Статус: {{ isActive ? 'Активен' : 'Не активен' }}</p>
  </div>
</template>

<style scoped>
div {
  border: 1px solid #ddd;
  padding: 10px;
  margin-top: 10px;
  border-radius: 5px;
  background-color: #f9f9f9;
}
</style>
