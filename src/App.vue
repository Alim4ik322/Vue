<script>
import InputText from './components/InputText.vue';
import SquareNumber from './components/SquareNumber.vue';
import UpperCaseText from './components/UpperCaseText.vue';
export default {
  name: 'App',
  components: {
      InputText,
      SquareNumber,
      UpperCaseText 

 }
}
</script>

<template>
  <div>
    <InputText/>
    <SquareNumber/>
    <UpperCaseText />
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
