<template>
  <div>
    <p v-if="isAdmin" class="admin-message">
      Вы вошли как администратор. У вас есть доступ ко всем функциям системы.
    </p>
    <p v-else class="user-message">
      Вы вошли как обычный пользователь. Доступ ограничен.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAdmin: true
    }
  }
}
</script>

<style scoped>
.admin-message {
  color: #2c3e50;
  background-color: #e8f5e9;
  padding: 15px;
  border-radius: 4px;
  border-left: 4px solid #4caf50;
}

.user-message {
  color: #2c3e50;
  background-color: #fff3e0;
  padding: 15px;
  border-radius: 4px;
  border-left: 4px solid #ff9800;
}
</style> 