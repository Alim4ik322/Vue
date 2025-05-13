<script>
export default {
  data() {
    return {
      text1: '',
      text2: ''
    }
  },
  methods: {
    swap() {
      [this.text1, this.text2] = [this.text2, this.text1]; // Меняем местами
    }
  }
}
</script>

<template>
  <div>
    <input v-model="text1" placeholder="Первый текст">
    <input v-model="text2" placeholder="Второй текст">
    <button @click="swap">Поменять местами</button>
  </div>
</template>
