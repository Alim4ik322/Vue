<template>
  <div>
    <button @click="showCurrentDay">Показать текущий день недели</button>
  </div>
</template>

<script>
export default {
  methods: {
    // Основной метод
    showCurrentDay: function() {
      let dayNumber = new Date().getDay();
      let dayName = this.getDayName(dayNumber);
      alert(dayName);
    },
    
    // Вспомогательный метод
    getDayName: function(dayNumber) {
      const days = ['Воскресенье', 'Понедельник', 'Вторник', 'Среда', 'Четверг', 'Пятница', 'Суббота'];
      return days[dayNumber];
    }
  }
}
</script> 