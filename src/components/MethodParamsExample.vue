<template>
  <div>
    <button @click="showSquare(2)">Квадрат числа 2</button>
    <button @click="showSquare(3)">Квадрат числа 3</button>
  </div>
</template>

<script>
export default {
  methods: {
    showSquare: function(num) {
      alert(num * num);
    }
  }
}
</script> 