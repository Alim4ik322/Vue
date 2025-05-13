<script>
export default {
  emits: ['firstAction', 'secondAction'] // Объявляем события
}
</script>

<template>
  <div>
    <button @click="$emit('firstAction')">Вызвать первую функцию</button>
    <button @click="$emit('secondAction')">Вызвать вторую функцию</button>
  </div>
</template>
