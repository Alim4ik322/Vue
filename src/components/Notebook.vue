<script>
export default {
  data() {
    return {
      notes: [
        { id: 1, title: 'Первая запись', content: 'Это моя первая заметка' },
        { id: 2, title: 'Вторая запись', content: 'А тут вторая запись' }
      ],
      selectedNote: null,
      searchQuery: ''
    }
  },
  computed: {
    filteredNotes() {
      return this.notes.filter(note =>
        note.title.toLowerCase().includes(this.searchQuery.toLowerCase())
      );
    }
  },
  methods: {
    addNote() {
      let newNote = { id: this.notes.length + 1, title: `Запись ${this.notes.length + 1}`, content: '' };
      this.notes.push(newNote);
      this.selectedNote = newNote;
    },
    deleteNote(id) {
      this.notes = this.notes.filter(note => note.id !== id);
      if (this.selectedNote && this.selectedNote.id === id) {
        this.selectedNote = null;
      }
    },
    updateNote() {
      let index = this.notes.findIndex(note => note.id === this.selectedNote.id);
      if (index !== -1) {
        this.notes[index] = this.selectedNote;
      }
    }
  }
}
</script>

<template>
  <div class="notebook">
    <h2>Блокнот</h2>
    <input v-model="searchQuery" placeholder="Поиск по заголовку...">
    <button @click="addNote">Добавить запись</button>

    <div class="container">
      <ul class="notes-list">
        <li v-for="note in filteredNotes" :key="note.id" @click="selectedNote = note">
          {{ note.title }}
          <button @click.stop="deleteNote(note.id)">Удалить</button>
        </li>
      </ul>

      <div v-if="selectedNote" class="editor">
        <input v-model="selectedNote.title" placeholder="Заголовок">
        <textarea v-model="selectedNote.content" placeholder="Текст записи"></textarea>
        <button @click="updateNote">Сохранить</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.notebook {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background: #f9f9f9;
  border-radius: 5px;
}

.container {
  display: flex;
}

.notes-list {
  width: 200px;
  list-style: none;
  padding: 0;
  margin: 10px;
}

.notes-list li {
  cursor: pointer;
  padding: 5px;
  background: #e0e0e0;
  margin-bottom: 5px;
  display: flex;
  justify-content: space-between;
}

.notes-list li:hover {
  background: #ccc;
}

.editor {
  flex: 1;
  padding: 10px;
}

input, textarea {
  display: block;
  width: 100%;
  margin-bottom: 10px;
  padding: 5px;
}

button {
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
