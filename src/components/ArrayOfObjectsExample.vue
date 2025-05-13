<template>
  <div>
    <!-- Список ссылок -->
    <h3>Список ссылок:</h3>
    <ul class="links-list">
      <li v-for="link in hrefs" :key="link.href" class="list-item">
        <a :href="link.href" class="link">{{ link.text }}</a>
      </li>
    </ul>

    <!-- Таблица продуктов -->
    <h3>Таблица продуктов:</h3>
    <table class="products-table">
      <thead>
        <tr>
          <th>Название</th>
          <th>Цена</th>
          <th>Количество</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.name" class="table-row">
          <td>{{ product.name }}</td>
          <td>{{ product.price }}</td>
          <td>{{ product.quantity }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hrefs: [
        { href: '1.html', text: 'text1' },
        { href: '2.html', text: 'text2' },
        { href: '3.html', text: 'text3' }
      ],
      products: [
        {
          name: 'product1',
          price: 100,
          quantity: 5
        },
        {
          name: 'product2',
          price: 200,
          quantity: 4
        },
        {
          name: 'product3',
          price: 300,
          quantity: 3
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

.links-list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 300px;
  margin: 0 auto;
}

.list-item {
  padding: 10px 20px;
  margin: 5px 0;
  background-color: #e3f2fd;
  border-radius: 4px;
  border-left: 4px solid #2196f3;
}

.link {
  color: #2196f3;
  text-decoration: none;
}

.link:hover {
  text-decoration: underline;
}

.products-table {
  width: 100%;
  max-width: 600px;
  margin: 20px auto;
  border-collapse: collapse;
  background-color: white;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.products-table th,
.products-table td {
  padding: 12px;
  text-align: left;
  border-bottom: 1px solid #e0e0e0;
}

.products-table th {
  background-color: #f5f5f5;
  font-weight: bold;
  color: #2c3e50;
}

.table-row:hover {
  background-color: #f8f9fa;
}
</style> 