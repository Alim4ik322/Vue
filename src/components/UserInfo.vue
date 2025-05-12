<template>
  <div>
    <div>{{ name }}</div>
    <div>{{ surn }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'johhn',
      surn: 'smit'
    }
  }
}
</script>

<style scoped>
div {
  margin: 10px 0;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style> 