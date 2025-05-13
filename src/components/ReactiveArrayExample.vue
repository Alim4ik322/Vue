<template>
  <div>
    <!-- Добавление элемента -->
    <h3>Добавление элемента:</h3>
    <ul class="list">
      <li v-for="(item, index) in addArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="addItem" class="button">Добавить элемент</button>

    <!-- Удаление первого элемента -->
    <h3>Удаление первого элемента:</h3>
    <ul class="list">
      <li v-for="(item, index) in removeFirstArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="removeFirst" class="button">Удалить первый</button>

    <!-- Удаление последнего элемента -->
    <h3>Удаление последнего элемента:</h3>
    <ul class="list">
      <li v-for="(item, index) in removeLastArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="removeLast" class="button">Удалить последний</button>

    <!-- Удаление предпоследнего элемента -->
    <h3>Удаление предпоследнего элемента:</h3>
    <ul class="list">
      <li v-for="(item, index) in removeSecondLastArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="removeSecondLast" class="button">Удалить предпоследний</button>

    <!-- Сортировка -->
    <h3>Сортировка:</h3>
    <ul class="list">
      <li v-for="(item, index) in sortArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="sortItems" class="button">Сортировать</button>

    <!-- Обратный порядок -->
    <h3>Обратный порядок:</h3>
    <ul class="list">
      <li v-for="(item, index) in reverseArray" :key="index" class="list-item">
        {{ item }}
      </li>
    </ul>
    <button @click="reverseItems" class="button">Обратный порядок</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      addArray: ['a', 'b', 'c'],
      removeFirstArray: ['a', 'b', 'c'],
      removeLastArray: ['a', 'b', 'c'],
      removeSecondLastArray: ['a', 'b', 'c'],
      sortArray: ['c', 'a', 'b'],
      reverseArray: ['a', 'b', 'c']
    }
  },
  methods: {
    addItem() {
      this.addArray.push('новый элемент')
    },
    removeFirst() {
      this.removeFirstArray.shift()
    },
    removeLast() {
      this.removeLastArray.pop()
    },
    removeSecondLast() {
      if (this.removeSecondLastArray.length >= 2) {
        this.removeSecondLastArray.splice(-2, 1)
      }
    },
    sortItems() {
      this.sortArray.sort()
    },
    reverseItems() {
      this.reverseArray.reverse()
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 300px;
  margin: 0 auto;
}

.list-item {
  padding: 10px 20px;
  margin: 5px 0;
  background-color: #e3f2fd;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
  text-align: left;
  font-size: 16px;
}

.button {
  background-color: #2196f3;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
  margin: 10px 0;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #1976d2;
}
</style> 