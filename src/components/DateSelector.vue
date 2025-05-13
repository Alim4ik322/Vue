<script>
export default {
  data() {
    return {
      selectedDay: '', 
      days: ['Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота', 'Воскресенье']
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите день недели:</h2>
    <select v-model="selectedDay">
      <option disabled value="">Выберите день</option>
      <option v-for="day in days" :key="day">{{ day }}</option>
    </select>
    <p v-if="selectedDay">Вы выбрали: {{ selectedDay }}</p>
  </div>
</template>
