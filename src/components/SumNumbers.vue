<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      sum: 0
    }
  },
  methods: {
    calc() {
      this.sum = this.num1 + this.num2; // Считаем сумму
    }
  }
}
</script>

<template>
  <div>
    <input v-model.number="num1" type="number" placeholder="Первое число">
    <input v-model.number="num2" type="number" placeholder="Второе число">
    <button @click="calc">Посчитать сумму</button>
    <p>Сумма чисел: {{ sum }}</p>
  </div>
</template>
