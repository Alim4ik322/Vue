<template>
  <div>
    <!-- Пример 1: Вывод значения из data -->
    <button @click="show">Показать текст</button>

    <!-- Пример 2: Сумма чисел из data -->
    <button @click="showSum">Показать сумму</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'str',
      num1: 1,
      num2: 2
    }
  },
  methods: {
    show: function() {
      alert(this.text);
    },
    showSum: function() {
      alert(this.num1 + this.num2);
    }
  }
}
</script> 