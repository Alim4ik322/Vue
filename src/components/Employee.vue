<script>
export default {
  props: ['name'], // Получаем имя работника
  emits: ['sendName'] // Объявляем событие
}
</script>

<template>
  <div>
    <p>Имя: {{ name }}</p>
    <button @click="$emit('sendName', name)">Передать имя</button>
  </div>
</template>
