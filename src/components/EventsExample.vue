<template>
  <div>
    <!-- Пример 1: Кнопка с выводом даты по клику -->
    <button @click="showDate">Показать дату</button>

    <!-- Пример 2: Кнопка с выводом даты по наведению -->
    <button @mouseover="showDate">Наведи на меня</button>
  </div>
</template>

<script>
export default {
  methods: {
    showDate: function() {
      alert(new Date().toLocaleString());
    }
  }
}
</script> 