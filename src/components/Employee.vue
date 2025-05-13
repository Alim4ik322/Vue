<script>
export default {
  props: {
    id: Number,
    name: String,
    salary: Number,
    age: Number
  },
  emits: ['update'], // Событие для обновления данных
  data() {
    return {
      isEdit: false, // Режим редактирования
      newName: this.name,
      newSalary: this.salary,
      newAge: this.age
    }
  },
  methods: {
    edit() {
      this.isEdit = true; // Включаем редактирование
    },
    save() {
      this.isEdit = false; // Сохраняем изменения и выключаем режим
      this.$emit('update', this.id, this.newName, this.newSalary, this.newAge);
    }
  }
}
</script>

<template>
  <div class="employee-card">
    <template v-if="!isEdit">
      <p><strong>Имя:</strong> {{ name }}</p>
      <p><strong>Зарплата:</strong> {{ salary }}</p>
      <p><strong>Возраст:</strong> {{ age }}</p>
      <button @click="edit">Редактировать</button>
    </template>
    <template v-else>
      <input v-model="newName" placeholder="Имя">
      <input v-model.number="newSalary" type="number" placeholder="Зарплата">
      <input v-model.number="newAge" type="number" placeholder="Возраст">
      <button @click="save">Сохранить</button>
    </template>
  </div>
</template>

<style scoped>
.employee-card {
  border: 1px solid #ddd;
  padding: 10px;
  margin: 10px 0;
  border-radius: 5px;
  background-color: #f9f9f9;
}
button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 5px 10px;
  cursor: pointer;
}
button:hover {
  background-color: #0056b3;
}
input {
  display: block;
  margin: 5px 0;
  padding: 5px;
}
</style>
