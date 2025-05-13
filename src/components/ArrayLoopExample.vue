<template>
  <div>
    <!-- Простой перебор элементов -->
    <h3>Простой перебор элементов:</h3>
    <div v-for="item in items" :key="item" class="item-box">
      {{ item }}
    </div>

    <!-- Вывод квадратов элементов -->
    <h3>Квадраты элементов:</h3>
    <div v-for="item in items" :key="item" class="item-box square">
      {{ item * item }}
    </div>

    <!-- Вывод в виде списка -->
    <h3>Элементы в виде списка:</h3>
    <ul class="items-list">
      <li v-for="item in items" :key="item" class="list-item">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5]
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.item-box {
  display: inline-block;
  padding: 10px 20px;
  margin: 5px;
  background-color: #e3f2fd;
  border-radius: 4px;
  border: 1px solid #2196f3;
}

.square {
  background-color: #e8f5e9;
  border-color: #4caf50;
}

.items-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.list-item {
  padding: 10px 20px;
  margin: 5px 0;
  background-color: #fff3e0;
  border-radius: 4px;
  border-left: 4px solid #ff9800;
}
</style> 