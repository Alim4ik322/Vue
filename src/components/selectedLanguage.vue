<script>
export default {
  data() {
    return {
      selectedLanguage: ''
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите язык:</h2>
    
    <label><input type="radio" v-model="selectedLanguage" value="Русский"> Русский</label>
    <label><input type="radio" v-model="selectedLanguage" value="Английский"> Английский</label>
    <label><input type="radio" v-model="selectedLanguage" value="Французский"> Французский</label>

    <h3 v-if="selectedLanguage">Фраза на выбранном языке:</h3>
    <p v-if="selectedLanguage === 'Русский'">Привет, как дела?</p>
    <p v-if="selectedLanguage === 'Английский'">Hello, how are you?</p>
    <p v-if="selectedLanguage === 'Французский'">Bonjour, comment ça va?</p>
  </div>
</template>
