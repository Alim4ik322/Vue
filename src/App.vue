<script>
import ChildComponent from './components/ChildComponent.vue';
export default {
  name: 'App',
  components: {
   ChildComponent
 }, 
  methods: {
    firstFunction() {
      alert('Первая функция вызвана!');
    },
    secondFunction() {
      alert('Вторая функция вызвана!');
    }
  }
}
</script>

<template>
  <div>
     <h2>Главный компонент</h2>
    <ChildComponent @firstAction="firstFunction" @secondAction="secondFunction" />
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
