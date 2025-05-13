<script>
export default {
  data() {
    return {
      cssClasses: 'highlight bold-text' // Динамические классы
    }
  }
}
</script>

<template>
  <p :class="cssClasses">Этот абзац использует динамические классы</p>
</template>

<style scoped>
  .highlight {
    color: red; /* Красный текст */
    background-color: yellow; /* Желтый фон */
  }
  .bold-text {
    font-weight: bold;
    font-size: 20px;
  }
</style>
