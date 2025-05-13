<script>
import DateSelector from './components/DateSelector.vue';
import WeekdaySelector from './components/WeekdaySelector.vue';
import FullDateSelector from './components/FullDateSelector.vue';
export default {
  name: 'App',
  components: {
     DateSelector,
     WeekdaySelector,
     FullDateSelector
 }
}
</script>

<template>
  <div>
  <DateSelector />
  <WeekdaySelector/>
  <FullDateSelector />


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
