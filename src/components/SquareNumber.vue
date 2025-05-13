<script>
export default {
  data() {
    return {
      number: 0 // Изначально 0
    }
  }
}
</script>

<template>
  <div>
    <input v-model.number="number" type="number"> <!-- Привязываем число -->
    <p>{{ number * number }}</p> <!-- Вычисляем квадрат -->
  </div>
</template>
