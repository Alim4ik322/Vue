<script>
export default {
  data() {
    return {
      nativeLanguage: '' // Хранит выбранный язык
    }
  }
}
</script>

<template>
  <div>
    <h2>Выберите ваш родной язык:</h2>
    
    <label><input type="radio" v-model="nativeLanguage" value="Русский"> Русский</label>
    <label><input type="radio" v-model="nativeLanguage" value="Английский"> Английский</label>
    <label><input type="radio" v-model="nativeLanguage" value="Французский"> Французский</label>

    <p v-if="nativeLanguage">Ваш родной язык: {{ nativeLanguage }}</p>
  </div>
</template>
