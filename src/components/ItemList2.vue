<script>
export default {
  data() {
    return {
      newItem: '',
      items: ['a', 'b', 'c', 'd', 'e']
    }
  },
  methods: {
    addItem() {
      if (this.newItem.trim() !== '') {
        this.items.unshift(this.newItem); // Добавляем в начало массива
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
