<script>
export default {
  data() {
    return {
      num: 0,
      res: 0
    }
  },
  methods: {
    calc() {
      this.res = Math.sqrt(this.num); // Вычисляем квадратный корень
    }
  }
}
</script>

<template>
  <div>
    <input v-model.number="num" type="number" placeholder="Введите число">
    <button @click="calc">Посчитать корень</button>
    <p>Квадратный корень: {{ res }}</p>
  </div>
</template>
