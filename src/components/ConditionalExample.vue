<template>
  <div>
    <p v-if="visible">Этот текст виден, когда visible = true</p>
    <p v-if="!visible">Этот текст виден, когда visible = false</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: true
    }
  }
}
</script> 