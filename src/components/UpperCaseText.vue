<script>
export default {
  data() {
    return {
      message: ''
    }
  }
}
</script>

<template>
  <div>
    <input v-model="message">
    <p>{{ message.toUpperCase() }}</p> <!-- Преобразование в верхний регистр -->
  </div>
</template>
