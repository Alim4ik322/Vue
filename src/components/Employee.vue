<script>
export default {
  data() {
    return {
      name: 'Алим',
      position: 'Разработчик'
    }
  }
}
</script>

<template>
  <div>
    <h3>Информация о сотруднике</h3>
    <p>Имя: {{ name }}</p>
    <p>Должность: {{ position }}</p>
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
