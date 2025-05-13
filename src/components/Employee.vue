<script>
export default {
  props: {
    id: Number,
    name: String,
    salary: Number,
    age: Number
  },
  emits: ['remove'] // Испускаем событие удаления
}
</script>

<template>
  <div class="employee-card">
    <p><strong>Имя:</strong> {{ name }}</p>
    <p><strong>Зарплата:</strong> {{ salary }}</p>
    <p><strong>Возраст:</strong> {{ age }}</p>
    <button @click="$emit('remove', id)">Удалить</button>
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
button {
  background-color: red;
  color: white;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
}
button:hover {
  background-color: darkred;
}
</style>
