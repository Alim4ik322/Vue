<script>
import ItemList1 from './components/ItemList1.vue';
import ItemList2 from './components/ItemList2.vue';


export default {
  name: 'App',
  components: {
   ItemList1,
   ItemList2
 }
}
</script>

<template>
  <div>
    <ItemList1/>
    <ItemList2/>
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
