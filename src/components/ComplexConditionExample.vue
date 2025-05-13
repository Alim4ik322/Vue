<template>
  <div>
    <p v-if="day === 'понедельник'" class="day-message monday">
      Сегодня понедельник
    </p>
    <p v-if="day === 'вторник'" class="day-message tuesday">
      Сегодня вторник
    </p>
    <p v-if="day === 'среда'" class="day-message wednesday">
      Сегодня среда
    </p>
    <p v-if="day === 'четверг'" class="day-message thursday">
      Сегодня четверг
    </p>
    <p v-if="day === 'пятница'" class="day-message friday">
      Сегодня пятница
    </p>
    <p v-if="day === 'суббота'" class="day-message saturday">
      Сегодня суббота
    </p>
    <p v-if="day === 'воскресенье'" class="day-message sunday">
      Сегодня воскресенье
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      day: 'понедельник'
    }
  }
}
</script>

<style scoped>
.day-message {
  padding: 15px;
  border-radius: 4px;
  margin: 10px 0;
  font-weight: bold;
}

.monday {
  background-color: #e3f2fd;
  border-left: 4px solid #2196f3;
}

.tuesday {
  background-color: #e8f5e9;
  border-left: 4px solid #4caf50;
}

.wednesday {
  background-color: #fff3e0;
  border-left: 4px solid #ff9800;
}

.thursday {
  background-color: #f3e5f5;
  border-left: 4px solid #9c27b0;
}

.friday {
  background-color: #e8eaf6;
  border-left: 4px solid #3f51b5;
}

.saturday {
  background-color: #fce4ec;
  border-left: 4px solid #e91e63;
}

.sunday {
  background-color: #fbe9e7;
  border-left: 4px solid #ff5722;
}
</style> 