<script>
import ClickableList from './components/ClickableList.vue';

export default {
  name: 'App',
  components: {
   ClickableList
 }
}
</script>

<template>
  <div>
    <ClickableList/>
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
