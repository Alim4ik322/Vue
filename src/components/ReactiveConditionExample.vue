<template>
  <div>
    <!-- Абзац с условным отображением -->
    <p v-if="visible">Этот текст можно показывать и скрывать</p>

    <!-- Кнопки для управления видимостью -->
    <button v-if="!visible" @click="show">Показать текст</button>
    <button v-if="visible" @click="hide">Скрыть текст</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false
    }
  },
  methods: {
    show: function() {
      this.visible = true;
    },
    hide: function() {
      this.visible = false;
    }
  }
}
</script> 