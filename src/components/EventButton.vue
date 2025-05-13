<script>
export default {
  emits: ['customEvent'] // Объявляем событие
}
</script>

<template>
  <button @click="$emit('customEvent')">
    Нажми меня
  </button>
</template>
