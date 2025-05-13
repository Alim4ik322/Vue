<script>
export default {
  data() {
    return {
      isDisabled: true // Изначально инпут заблокирован
    }
  },
  methods: {
    toggleInput() {
      this.isDisabled = !this.isDisabled; // Меняем состояние при клике
    }
  }
}
</script>

<template>
  <div>
    <input :disabled="isDisabled" placeholder="Введите текст">
    <button @click="toggleInput">{{ isDisabled ? 'Разблокировать' : 'Заблокировать' }}</button>
  </div>
</template>
