<script>
export default {
  data() {
    return {
      clickMessage: ''
    }
  },
  methods: {
    handleMouseClick(event) {
      if (event.button === 0) {
        this.clickMessage = 'left';
      } else if (event.button === 1) {
        this.clickMessage = 'middle';
      } else if (event.button === 2) {
        this.clickMessage = 'right';
      }
    }
  }
}
</script>

<template>
  <div>
    <a href="#" @mousedown="handleMouseClick">Кликните сюда</a>
    <p v-if="clickMessage">Вы нажали: {{ clickMessage }}</p>
  </div>
</template>
