<script>
import StyledText from './components/StyledText.vue';

export default {
  name: 'App',
  components: {
    StyledText
  }
}
</script>

<template>
  <div>
         <StyledText />
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
