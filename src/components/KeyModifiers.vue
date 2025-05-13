<script>
export default {
  data() {
    return {
      inputText: '', // Введенный текст
      displayedText: '' // Выводимый текст
    }
  },
  methods: {
    updateText() {
      this.displayedText = this.inputText; // Устанавливаем текст
    }
  }
}
</script>

<template>
  <div>
    <input v-model="inputText" @keydown.enter="updateText" placeholder="Введите текст и нажмите Enter">
    <p v-if="displayedText">Вы ввели: {{ displayedText }}</p>
  </div>
</template>
