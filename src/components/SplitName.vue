<script>
export default {
  data() {
    return {
      fullName: '',
      surname: '',
      name: '',
      patronymic: ''
    }
  },
  methods: {
    splitName() {
      const parts = this.fullName.split(' ');
      [this.surname, this.name, this.patronymic] = parts.length === 3 ? parts : ['', '', ''];
    }
  }
}
</script>

<template>
  <div>
    <input v-model="fullName" placeholder="Введите ФИО">
    <button @click="splitName">Разделить ФИО</button>
    <p>Фамилия: {{ surname }}</p>
    <p>Имя: {{ name }}</p>
    <p>Отчество: {{ patronymic }}</p>
  </div>
</template>
