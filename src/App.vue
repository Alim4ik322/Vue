<script>
import SquareRoot from './components/SquareRoot.vue';
import SumNumbers from './components/SumNumbers.vue';
import SwapText from './components/SwapText.vue';
import SplitName from './components/SplitName.vue';
export default {
  name: 'App',
  components: {
      SquareRoot,
      SumNumbers,
      SwapText,
      SplitName

 }
}
</script>

<template>
  <div>
    <SquareRoot/>
    <SumNumbers/>
    <SwapText/>
    <SplitName/>
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
