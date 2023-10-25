<template>
  <nav :class="{ 'openNav': isNavOpen }">
    <a href="">Обо мне</a>
    <a href="">Образование</a>
    <a href="">Мои работы</a>
    <a href="">Контакты</a>
  </nav>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    data() {
      return {
        isNavOpen: false,
      };
    },
    mounted() {
      setTimeout(() => {
        this.isNavOpen = true;
      }, 700);
    },
  });
</script>




<style scoped lang="scss">
  nav {
    display: flex;
    justify-content: center;
    gap: 40px;
    width: 100%;
    box-shadow: 0 0 15px 0 rgba(0, 0, 0, 0.473);
    padding: 10px;
    width: 100vw;
    font-weight: bold;
    position: fixed;
    z-index: 10;
    background-color: #fff;
    transform: translateY(-100%);
    transition: transform 0.5s ease-in-out;

    a {
      text-decoration: none;
      color: black;
      &:hover {
        color: rgb(53, 31, 250);
        transition: 0.5s;
      }
    }

    @media (max-width: 550px) {
      gap: 12px;
      font-size: 14px;
    }
  }
  .openNav {
      transform: translateY(0);
  }
</style>

