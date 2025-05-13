<template>
  <p :class="{ active: true, valid: false }">Этот текст использует инлайн-объект классов</p>
</template>

<style scoped>
  .active {
    color: green;
    font-weight: bold;
  }

  .valid {
    text-decoration: underline;
    color: blue;
  }
</style>
