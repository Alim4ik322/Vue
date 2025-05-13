<template>
  <div>
    <!-- Первый абзац и кнопка -->
    <div class="toggle-group">
      <button @click="toggleFirst">
        {{ firstVisible ? 'Скрыть первый абзац' : 'Показать первый абзац' }}
      </button>
      <p v-if="firstVisible">Первый абзац</p>
    </div>

    <!-- Второй абзац и кнопка -->
    <div class="toggle-group">
      <button @click="toggleSecond">
        {{ secondVisible ? 'Скрыть второй абзац' : 'Показать второй абзац' }}
      </button>
      <p v-if="secondVisible">Второй абзац</p>
    </div>

    <!-- Третий абзац и кнопка -->
    <div class="toggle-group">
      <button @click="toggleThird">
        {{ thirdVisible ? 'Скрыть третий абзац' : 'Показать третий абзац' }}
      </button>
      <p v-if="thirdVisible">Третий абзац</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstVisible: false,
      secondVisible: false,
      thirdVisible: false
    }
  },
  methods: {
    toggleFirst() {
      this.firstVisible = !this.firstVisible;
    },
    toggleSecond() {
      this.secondVisible = !this.secondVisible;
    },
    toggleThird() {
      this.thirdVisible = !this.thirdVisible;
    }
  }
}
</script>

<style scoped>
.toggle-group {
  margin: 20px 0;
}

button {
  margin-right: 10px;
  padding: 5px 10px;
  cursor: pointer;
  min-width: 200px;
}

p {
  display: inline-block;
  margin: 0;
  padding: 5px;
  background-color: #f0f0f0;
  border-radius: 4px;
}
</style> 