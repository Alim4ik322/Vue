<script>
export default {
  props: ['name', 'salary'], // Получаем данные о работнике
  emits: ['sendData']
}
</script>

<template>
  <div>
    <p>Имя: {{ name }}</p>
    <p>Зарплата: {{ salary }}</p>
    <button @click="$emit('sendData', name, salary)">Передать данные</button>
  </div>
</template>
