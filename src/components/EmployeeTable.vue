<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30, isEdit: false },
        { id: 2, name: 'name2', salary: 200, age: 40, isEdit: false },
        { id: 3, name: 'name3', salary: 300, age: 50, isEdit: false }
      ]
    }
  },
  methods: {
    editUser(user) {
      user.isEdit = true; // Включаем режим редактирования
    },
    saveUser(user) {
      user.isEdit = false; // Сохраняем изменения и выключаем редактирование
    },
    removeUser(id) {
      this.users = this.users.filter(user => user.id !== id);
    }
  }
}
</script>

<template>
  <div>
    <h2>Список работников</h2>
    <table border="1">
      <thead>
        <tr>
          <th>ID</th>
          <th>Имя</th>
          <th>Зарплата</th>
          <th>Возраст</th>
          <th>Действия</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{ user.id }}</td>
          <td>
            <template v-if="!user.isEdit">
              {{ user.name }}
            </template>
            <template v-else>
              <input v-model="user.name">
            </template>
          </td>
          <td>
            <template v-if="!user.isEdit">
              {{ user.salary }}
            </template>
            <template v-else>
              <input v-model.number="user.salary" type="number">
            </template>
          </td>
          <td>
            <template v-if="!user.isEdit">
              {{ user.age }}
            </template>
            <template v-else>
              <input v-model.number="user.age" type="number">
            </template>
          </td>
          <td>
            <template v-if="!user.isEdit">
              <a href="#" @click.prevent="editUser(user)">Редактировать</a> |
              <a href="#" @click.prevent="removeUser(user.id)" style="color: red;">Удалить</a>
            </template>
            <template v-else>
              <button @click="saveUser(user)">Сохранить</button>
            </template>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 10px;
}

th, td {
  padding: 10px;
  text-align: center;
}

th {
  background-color: #f4f4f4;
}

a {
  color: blue;
  cursor: pointer;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

button {
  padding: 5px 10px;
  cursor: pointer;
}
</style>
