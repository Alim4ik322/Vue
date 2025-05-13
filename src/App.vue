<script>
import VisibilityComponent from './components/VisibilityComponent.vue';
export default {
  name: 'App',
  components: {
    VisibilityComponent
  }
}
</script>

<template>
  <div>
        <VisibilityComponent />
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
