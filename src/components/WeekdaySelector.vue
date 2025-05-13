<script>
export default {
  data() {
    return {
      selectedDay: '',
      selectedMonth: '',
      selectedYear: '',
      days: Array.from({ length: 31 }, (_, i) => i + 1),
      months: ['Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь'],
      years: Array.from({ length: 50 }, (_, i) => new Date().getFullYear() - i)
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите дату:</h2>
    <select v-model="selectedDay">
      <option disabled value="">День</option>
      <option v-for="day in days" :key="day">{{ day }}</option>
    </select>

    <select v-model="selectedMonth">
      <option disabled value="">Месяц</option>
      <option v-for="month in months" :key="month">{{ month }}</option>
    </select>

    <select v-model="selectedYear">
      <option disabled value="">Год</option>
      <option v-for="year in years" :key="year">{{ year }}</option>
    </select>

    <p v-if="selectedDay && selectedMonth && selectedYear">
      Вы выбрали: {{ selectedDay }} {{ selectedMonth }} {{ selectedYear }}
    </p>
  </div>
</template>
