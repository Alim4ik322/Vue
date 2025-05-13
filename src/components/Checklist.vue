<script>
export default {
  data() {
    return {
      tasks: [
        { id: 1, text: 'Купить продукты', done: false },
        { id: 2, text: 'Сделать зарядку', done: false },
        { id: 3, text: 'Прочитать книгу', done: true }
      ],
      newTask: ''
    }
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({ id: this.tasks.length + 1, text: this.newTask, done: false });
        this.newTask = '';
      }
    },
    removeTask(id) {
      this.tasks = this.tasks.filter(task => task.id !== id);
    },
    toggleTask(id) {
      this.tasks = this.tasks.map(task => {
        if (task.id === id) task.done = !task.done;
        return task;
      });
    },
    editTask(id, newText) {
      this.tasks = this.tasks.map(task => {
        if (task.id === id) task.text = newText;
        return task;
      });
    }
  }
}
</script>

<template>
  <div class="checklist">
    <h2>Чеклист дел</h2>
    <input v-model="newTask" placeholder="Добавить новое дело">
    <button @click="addTask">Добавить</button>

    <ul>
      <li v-for="task in tasks" :key="task.id">
        <input type="checkbox" v-model="task.done" @change="toggleTask(task.id)">
        <span :class="{ done: task.done }">{{ task.text }}</span>
        <button @click="removeTask(task.id)">Удалить</button>
        <button @click="editTask(task.id, prompt('Введите новый текст', task.text))">Редактировать</button>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.checklist {
  max-width: 400px;
  margin: 0 auto;
  padding: 10px;
  background: #f9f9f9;
  border-radius: 5px;
}

input[type="checkbox"] {
  margin-right: 10px;
}

.done {
  text-decoration: line-through;
  color: gray;
}

button {
  margin-left: 5px;
  padding: 5px 10px;
  cursor: pointer;
  border: none;
  background: #007bff;
  color: white;
  border-radius: 3px;
}

button:hover {
  background: #0056b3;
}
</style>
