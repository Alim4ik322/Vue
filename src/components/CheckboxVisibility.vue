<script>
export default {
  data() {
    return {
      checked: false
    }
  }
}
</script>

<template>
  <div>
    <input type="checkbox" v-model="checked">
    <p v-if="checked">Этот абзац отображается, когда чекбокс включен</p>
  </div>
</template>
