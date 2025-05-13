<script>
import User from './components/User.vue';
export default {
  name: 'App',
  components: {
   User
 }
}
</script>

<template>
  <div>
     <h2>Главный компонент</h2>
    <User :items="itemList" />
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
