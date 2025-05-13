<script>
export default {
  data() {
    return {
      selectedCity: '' // Хранит выбранный город
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите ваш город:</h2>
    
    <select v-model="selectedCity">
      <option disabled value="">Выберите город</option>
      <option>Москва</option>
      <option>Нью-Йорк</option>
      <option>Лондон</option>
      <option>Токио</option>
      <option>Париж</option>
    </select>

    <p v-if="selectedCity">Вы живете в: {{ selectedCity }}</p>
  </div>
</template>

<style scoped>
select {
  padding: 5px;
  font-size: 16px;
  margin-top: 10px;
}
</style>
