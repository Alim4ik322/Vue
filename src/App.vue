<script>
import KeyModifiers from './components/KeyModifiers.vue';
import CtrlClick from './components/CtrlClick.vue';
import MouseClick from './components/MouseClick.vue';

export default {
  name: 'App',
  components: {
    KeyModifiers,
    CtrlClick,
    MouseClick
 }
}
</script>

<template>
  <div>
  <KeyModifiers />
  <CtrlClick />
  <MouseClick />
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
