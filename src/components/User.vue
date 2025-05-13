<script>
export default {
  props: ['items'] // Получаем массив от родителя
}
</script>

<template>
  <div>
    <h3>Список элементов:</h3>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>
