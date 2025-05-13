<template>
  <div>
    <h3>Ключи массива:</h3>
    <ul class="keys-list">
      <li v-for="(elem, key) in arr" :key="key" class="key-item">
        Ключ: {{ key }}, Значение: {{ elem }}
      </li>
    </ul>

    <h3>Ключи массива (начиная с 1):</h3>
    <ul class="keys-list">
      <li v-for="(elem, key) in arr" :key="key" class="key-item">
        Ключ: {{ key + 1 }}, Значение: {{ elem }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ['x', 'y', 'z']
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.keys-list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 300px;
  margin: 0 auto;
}

.key-item {
  padding: 10px 20px;
  margin: 5px 0;
  background-color: #e3f2fd;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
  text-align: left;
}
</style> 