<template>
  <div>
    <h3>Все элементы массива:</h3>
    <ul class="numbers-list">
      <li v-for="item in items" :key="item" class="list-item">
        {{ item }}
      </li>
    </ul>

    <h3>Только положительные элементы:</h3>
    <ul class="numbers-list">
      <template v-for="item in items" :key="item">
        <li v-if="item > 0" class="list-item positive">
          {{ item }}
        </li>
      </template>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, -2, 3, -4, 5]
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.numbers-list {
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
  text-align: center;
  font-size: 18px;
}

.list-item.positive {
  background-color: #e8f5e9;
  border-left-color: #4caf50;
  color: #2e7d32;
}
</style> 