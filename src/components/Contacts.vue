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
    display: flex;
    gap: 10px;
    max-width: 100vw;
    text-align: center;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
    align-items: center;

    a {
      text-decoration: none;
      color: black;
      margin: 0;
      padding: 0;
    }
    @media (max-width: 550px) {
        font-size: 12px;
        gap: 10px;
        width: 100%;
      }
  }
</style>

