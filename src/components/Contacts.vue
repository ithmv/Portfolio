<template>
  <div class="container">
    <a href="tel:+1234567890">+1 (234) 567-890</a>
    <a href="mailto:youremail@example.com">youremail@example.com</a>
    <a href="https://t.me/ithmv" target="_blank">Telegram</a>
    <a href="https://vk.com/ithmv" target="_blank">ВКонтакте</a>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
  });
</script>

<style scoped lang="scss">
  .container {
    width: 95%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 20px;
    text-align: center;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
  }
</style>

