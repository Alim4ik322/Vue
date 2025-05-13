<script>
export default {
  data() {
    return {
      items: ['a', 'b', 'c', 'd', 'e'] // Исходный массив
    }
  },
  methods: {
    removeItem(index) {
      this.items.splice(index, 1); // Удаление элемента по индексу
    }
  }
}
</script>

<template>
  <div>
    <h2>Нажмите на элемент, чтобы удалить его:</h2>
    <ul>
      <li v-for="(item, index) in items" :key="index" @click="removeItem(index)">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
li {
  cursor: pointer;
  padding: 5px;
  background-color: #f4f4f4;
  margin: 5px;
  border-radius: 5px;
}
li:hover {
  background-color: #e0e0e0;
}
</style>
