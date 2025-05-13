<script>
export default {
  props: ['name', 'salary', 'age'] // Получаем данные от родителя
}
</script>

<template>
  <div>
    <h3>Информация о сотруднике</h3>
    <p>Имя: {{ name }}</p>
    <p>Зарплата: {{ salary }}</p>
    <p>Возраст: {{ age }}</p>
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
