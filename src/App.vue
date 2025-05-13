<script>
import nativeLanguage from './components/nativeLanguage.vue';
import selectedLanguage from './components/selectedLanguage.vue';
export default {
  name: 'App',
  components: {
     selectedLanguage,
     nativeLanguage

 }
}
</script>

<template>
  <div>
   <nativeLanguage />
   <selectedLanguage/>
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
