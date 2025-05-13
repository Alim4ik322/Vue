<script>
export default {
  data() {
    return {
      newItem: '', // Текст из инпута
      items: ['a', 'b', 'c', 'd', 'e'] // Исходный массив
    }
  },
  methods: {
    addItem() {
      if (this.newItem.trim() !== '') {
        this.items.push(this.newItem); // Добавляем в конец массива
        this.newItem = ''; // Очищаем инпут
      }
    }
  }
}
</script>

<template>
  <div>
    <input v-model="newItem" placeholder="Введите новый элемент">
    <button @click="addItem">Добавить</button>
    
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>
