<template>
  <div>
    <p v-if="age < 18" class="age-message teenager">
      Подросток
    </p>
    <p v-else-if="age >= 18 && age <= 25" class="age-message young">
      Молодой человек
    </p>
    <p v-else class="age-message adult">
      Мужчина
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: 25
    }
  }
}
</script>

<style scoped>
.age-message {
  padding: 15px;
  border-radius: 4px;
  margin: 10px 0;
  font-weight: bold;
}

.teenager {
  background-color: #e3f2fd;
  border-left: 4px solid #2196f3;
}

.young {
  background-color: #e8f5e9;
  border-left: 4px solid #4caf50;
}

.adult {
  background-color: #fff3e0;
  border-left: 4px solid #ff9800;
}
</style> 