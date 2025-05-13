<template>
  <div>
    <!-- Пример 1: Сложение двух чисел -->
    <div>
      <h3>Пример 1: Сложение двух чисел</h3>
      <p>var1 + var2 = {{ var1 + var2 }}</p>
    </div>

    <!-- Пример 2: Возведение в квадрат -->
    <div>
      <h3>Пример 2: Квадрат числа</h3>
      <p>Квадрат числа {{ num }} = {{ num * num }}</p>
    </div>

    <!-- Пример 3: Сумма трех чисел -->
    <div>
      <h3>Пример 3: Сумма трех чисел</h3>
      <p>num1 + num2 + num3 = {{ num1 + num2 + num3 }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CalculationsExample',
  data() {
    return {
      // Данные для примера 1
      var1: 1,
      var2: 2,

      // Данные для примера 2
      num: 5,

      // Данные для примера 3
      num1: 1,
      num2: 2,
      num3: 3
    }
  }
}
</script> 