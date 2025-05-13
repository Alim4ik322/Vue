<template>
  <div>
    <!-- Вывод значений свойств -->
    <p>Цена продукта: {{ cost }}</p>
    <p>Количество: {{ amount }}</p>
    <p>Общая стоимость: {{ price }}</p>

    <!-- Кнопка для изменения цены -->
    <button @click="changeCost">Изменить цену</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cost: 100,
      amount: 5
    }
  },
  computed: {
    price: function() {
      return this.cost * this.amount;
    }
  },
  methods: {
    changeCost: function() {
      this.cost = 200;
    }
  }
}
</script> 