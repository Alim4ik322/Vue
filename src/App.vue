<script>
import EventButton from './components/EventButton.vue';
export default {
  name: 'App',
  components: {
   EventButton
 }, 
  methods: {
    handleEvent() {
      alert('Событие испущено!');
    }
  }
}
</script>

<template>
  <div>
    <h2>Главный компонент</h2>
    <EventButton @customEvent="handleEvent" />
  </div>
</template>

<style>
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
