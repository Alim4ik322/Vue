<script>
export default {
  data() {
    return {
      isEnabled: false // По умолчанию инпут заблокирован
    }
  }
}
</script>

<template>
  <div>
    <label>
      <input type="checkbox" v-model="isEnabled">
      Разблокировать инпут
    </label>
    <input :disabled="!isEnabled" placeholder="Введите текст">
  </div>
</template>
