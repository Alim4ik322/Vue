<script>
export default {
  data() {
    return {
      obj: {
        hidden: true
      }
    }
  },
  methods: {
    showElement() {
      this.obj.hidden = false;
    },
    hideElement() {
      this.obj.hidden = true;
    },
    toggleElement() {
      this.obj.hidden = !this.obj.hidden;
    }
  }
}
</script>

<template>
  <div>
    <p :class="obj">Этот текст можно скрыть или показать</p>
    <button @click="showElement">Показать</button>
    <button @click="hideElement">Скрыть</button>
    <button @click="toggleElement">Тогглить</button>
  </div>
</template>

<style scoped>
  .hidden {
    display: none;
  }
</style>
