<script>
export default {
  data() {
    return {
      selectedDay: new Date().getDate(),
      selectedMonth: new Date().toLocaleString('ru-RU', { month: 'long' }),
      selectedYear: new Date().getFullYear(),
      days: Array.from({ length: 31 }, (_, i) => i + 1),
      months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      years: Array.from({ length: 50 }, (_, i) => new Date().getFullYear() - i)
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите дату (текущая дата выбрана по умолчанию):</h2>
    <select v-model="selectedDay">
      <option v-for="day in days" :key="day">{{ day }}</option>
    </select>

    <select v-model="selectedMonth">
      <option v-for="month in months" :key="month">{{ month }}</option>
    </select>

    <select v-model="selectedYear">
      <option v-for="year in years" :key="year">{{ year }}</option>
    </select>

    <p>Вы выбрали: {{ selectedDay }} {{ selectedMonth }} {{ selectedYear }}</p>
  </div>
</template>
