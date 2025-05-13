<script>
import StyledParagraph from './components/StyledParagraph.vue';

export default {
  name: 'App',
  components: {
        StyledParagraph
  }
}
</script>

<template>
  <div>
      <StyledParagraph />
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
