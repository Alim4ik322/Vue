<script>
export default {
  data() {
    return {
      message: '' // Изначально пустая строка
    }
  }
}
</script>

<template>
  <div>
    <input v-model="message">
    <p>{{ message }}</p>
  </div>
</template>
