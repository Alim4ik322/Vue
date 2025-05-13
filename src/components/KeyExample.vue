<template>
  <div>
    <h3>Список продуктов:</h3>
    <ul class="products-list">
      <li v-for="product in products" :key="product.id" class="product-item">
        {{ product.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'product1'
        },
        {
          id: 2,
          name: 'product2'
        },
        {
          id: 3,
          name: 'product3'
        }
      ]
    }
  }
}
</script>

<style scoped>
h3 {
  color: #2c3e50;
  margin: 20px 0 10px;
}

.products-list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 300px;
  margin: 0 auto;
}

.product-item {
  padding: 12px 20px;
  margin: 8px 0;
  background-color: #e3f2fd;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
  text-align: left;
  font-size: 16px;
  transition: all 0.3s ease;
}

.product-item:hover {
  background-color: #bbdefb;
  transform: translateX(5px);
}
</style> 