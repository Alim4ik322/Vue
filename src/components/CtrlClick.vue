<script>
export default {
  data() {
    return {
      message: '' // Текст для абзаца
    }
  },
  methods: {
    handleClick(event) {
      if (event.ctrlKey) {
        this.message = 'Клик с Ctrl!';
      }
    }
  }
}
</script>

<template>
  <div>
    <a href="#" @click.prevent="handleClick">Нажмите, удерживая Ctrl</a>
    <p v-if="message">{{ message }}</p>
  </div>
</template>
