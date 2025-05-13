<script>
export default {
  data() {
    return {
      selectedLanguages: [] // Массив выбранных языков
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите языки, которые вы знаете:</h2>
    
    <label><input type="checkbox" v-model="selectedLanguages" value="Русский"> Русский</label>
    <label><input type="checkbox" v-model="selectedLanguages" value="Английский"> Английский</label>
    <label><input type="checkbox" v-model="selectedLanguages" value="Французский"> Французский</label>
    <label><input type="checkbox" v-model="selectedLanguages" value="Немецкий"> Немецкий</label>
    <label><input type="checkbox" v-model="selectedLanguages" value="Испанский"> Испанский</label>

    <h3>Выбранные языки:</h3>
    <ul>
      <li v-for="(language, index) in selectedLanguages" :key="index">{{ language }}</li>
    </ul>
  </div>
</template>

<style scoped>
label {
  display: block;
  margin: 5px 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  background-color: #f4f4f4;
  padding: 5px;
  margin: 2px;
  border-radius: 5px;
}
</style>
