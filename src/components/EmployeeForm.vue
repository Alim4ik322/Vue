<script>
export default {
  emits: ['add'], // Испускаем событие добавления
  data() {
    return {
      newName: '',
      newSalary: null,
      newAge: null
    }
  },
  methods: {
    save() {
      if (this.newName.trim() !== '' && this.newSalary && this.newAge) {
        this.$emit('add', this.newName, this.newSalary, this.newAge);
        this.newName = '';
        this.newSalary = null;
        this.newAge = null;
      }
    }
  }
}
</script>

<template>
  <div class="form-container">
    <h3>Добавить нового сотрудника</h3>
    <input v-model="newName" placeholder="Имя">
    <input v-model.number="newSalary" type="number" placeholder="Зарплата">
    <input v-model.number="newAge" type="number" placeholder="Возраст">
    <button @click="save">Добавить</button>
  </div>
</template>

<style scoped>
.form-container {
  border: 1px solid #ddd;
  padding: 10px;
  margin-top: 10px;
  border-radius: 5px;
  background-color: #f9f9f9;
}
input {
  display: block;
  margin: 5px 0;
  padding: 5px;
}
button {
  background-color: #28a745;
  color: white;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
}
button:hover {
  background-color: #218838;
}
</style>
