<script>
export default {
  data() {
    return {
      isValid: true,   // Указывает, что элемент валидный
      isDisabled: true // Указывает, что элемент отключен
    }
  }
}
</script>

<template>
  <p :class="{ valid: isValid, disabled: isDisabled }">
    Этот элемент получает классы динамически
  </p>
</template>

<style scoped>
  .valid {
    color: green; /* Применится, если isValid = true */
    font-weight: bold;
  }

  .disabled {
    color: gray; /* Применится, если isDisabled = true */
    opacity: 0.6;
    pointer-events: none;
  }
</style>
