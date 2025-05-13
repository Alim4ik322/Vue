<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 }
      ]
    }
  },
  methods: {
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
          <th>Действие</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" :key="user.id">
          <td>{{ user.id }}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.salary }}</td>
          <td>{{ user.age }}</td>
          <td><a href="#" @click.prevent="removeUser(user.id)">Удалить</a></td>
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
  color: red;
  cursor: pointer;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>
