<template>
  <div>
    <p v-if="!hidden">text</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hidden: true
    }
  }
}
</script> 