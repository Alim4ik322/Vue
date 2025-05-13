<template>
  <div>
    <!-- Пример с изображением -->
    <img :src="attr">
    
    <!-- Пример со ссылкой -->
    <a :href="href">{{ text }}</a>
  </div>
</template>

<script>
export default {
  name: 'AttributesExample',
  data() {
    return {
      // Данные для изображения
      attr: 'img.png',
      
      // Данные для ссылки
      text: 'page',
      href: 'page.html'
    }
  }
}
</script> 