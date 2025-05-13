<script>
export default {
  data() {
    return {
      obj: {
        done: true,
        selected: false
      }
    }
  }
}
</script>

<template>
  <p :class="obj">Проверка CSS классов</p>
</template>

<style scoped>
  .done {
    color: green;
    font-weight: bold;
  }

  .selected {
    color: blue;
    text-decoration: underline;
  }
</style>
