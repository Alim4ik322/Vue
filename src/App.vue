<script>
import UserInfo from './components/UserInfo.vue'
import AttributesExample from './components/AttributesExample.vue'
import CalculationsExample from './components/CalculationsExample.vue'
import ArraysExample from './components/ArraysExample.vue'

export default {
  name: 'App',
  components: {
    UserInfo,
    AttributesExample,
    CalculationsExample,
    ArraysExample
  }
}
</script>

<template>
  <div>
    <UserInfo />
    <AttributesExample />
    <CalculationsExample />
    <ArraysExample />
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
