<template>
  <div>
    <!-- Ссылка с предотвращением перехода -->
    <a href="https://example.com" @click.prevent="handleClick">Нажми меня</a>

    <!-- Кнопка с однократным срабатыванием -->
    <button @click.once="handleClick">Нажми меня один раз</button>
  </div>
</template>

<script>
export default {
  methods: {
    handleClick: function() {
      alert('Событие сработало!');
    }
  }
}
</script> 