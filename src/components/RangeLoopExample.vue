<template>
  <div>
    <h3>Числа от 1 до 30:</h3>
    <div class="numbers-grid">
      <p v-for="num in 30" :key="num" class="number-item">
        {{ num }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RangeLoopExample'
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.numbers-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 10px;
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

.number-item {
  background-color: #e3f2fd;
  padding: 15px;
  border-radius: 4px;
  text-align: center;
  font-size: 18px;
  color: #2196f3;
  border: 1px solid #bbdefb;
  margin: 0;
  transition: all 0.3s ease;
}

.number-item:hover {
  background-color: #bbdefb;
  transform: scale(1.05);
}
</style> 