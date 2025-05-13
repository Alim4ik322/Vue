<template>
  <div>
    <!-- Простой перебор значений -->
    <h3>Только значения:</h3>
    <ul class="users-list">
      <li v-for="value in users" :key="value" class="list-item">
        {{ value }}
      </li>
    </ul>

    <!-- Перебор ключей и значений -->
    <h3>Ключи и значения:</h3>
    <ul class="users-list">
      <li v-for="(value, key) in users" :key="key" class="list-item">
        {{ key }} - {{ value }}
      </li>
    </ul>

    <!-- Перебор с индексами (начиная с 0) -->
    <h3>Ключи, значения и индексы (с 0):</h3>
    <ul class="users-list">
      <li v-for="(value, key, index) in users" :key="key" class="list-item">
        {{ key }} - {{ value }} - {{ index }}
      </li>
    </ul>

    <!-- Перебор с индексами (начиная с 1) -->
    <h3>Ключи, значения и индексы (с 1):</h3>
    <ul class="users-list">
      <li v-for="(value, key, index) in users" :key="key" class="list-item">
        {{ key }} - {{ value }} - {{ index + 1 }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: {
        user1: '100$',
        user2: '200$',
        user3: '300$'
      }
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.users-list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 400px;
  margin: 0 auto;
}

.list-item {
  padding: 10px 20px;
  margin: 5px 0;
  background-color: #e3f2fd;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
  text-align: left;
}
</style> 