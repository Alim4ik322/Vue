<template>
  <div>
    <button @click="toggleVisibility" class="toggle-button">
      {{ isVisible ? 'Скрыть абзацы' : 'Показать абзацы' }}
    </button>

    <template v-if="isVisible">
      <p class="paragraph">Первый абзац</p>
      <p class="paragraph">Второй абзац</p>
      <p class="paragraph">Третий абзац</p>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: true
    }
  },
  methods: {
    toggleVisibility() {
      this.isVisible = !this.isVisible;
    }
  }
}
</script>

<style scoped>
.toggle-button {
  padding: 10px 20px;
  margin-bottom: 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 16px;
}

.toggle-button:hover {
  background-color: #45a049;
}

.paragraph {
  padding: 15px;
  margin: 10px 0;
  background-color: #f5f5f5;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
}
</style> 