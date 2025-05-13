<template>
  <div>
    <!-- Вывод значения свойства text -->
    <p>Текущее значение: {{ text }}</p>

    <!-- Кнопка для изменения значения -->
    <button @click="changeText">Изменить текст</button>

    <!-- Две кнопки для разных значений -->
    <button @click="setText1">Установить текст 1</button>
    <button @click="setText2">Установить текст 2</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: 'xxx'
    }
  },
  methods: {
    changeText: function() {
      this.text = 'yyy';
    },
    setText1: function() {
      this.text = 'первый текст';
    },
    setText2: function() {
      this.text = 'второй текст';
    }
  }
}
</script> 