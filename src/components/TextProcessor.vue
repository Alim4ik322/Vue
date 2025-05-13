<script>
export default {
  data() {
    return {
      text: '', // Исходный текст из textarea
      words: [] // Массив слов
    }
  },
  methods: {
    processText() {
      this.words = this.text.split(' ').filter(word => word.trim() !== ''); // Разбиваем текст по пробелам, убираем пустые строки
    }
  }
}
</script>

<template>
  <div>
    <h2>Обработчик текста</h2>
    <textarea v-model="text" placeholder="Введите текст"></textarea>
    <button @click="processText">Разбить на слова</button>
    <ul>
      <li v-for="(word, index) in words" :key="index">{{ word }}</li>
    </ul>
  </div>
</template>

<style scoped>
textarea {
  width: 100%;
  height: 100px;
  padding: 10px;
  font-size: 16px;
  margin-bottom: 10px;
}

button {
  display: block;
  margin: 10px auto;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background-color: #f4f4f4;
  margin: 5px;
  padding: 10px;
  border-radius: 5px;
}
</style>
