<template>
   <Header />
  <section>
    <About v-for="item in data" :key="item.id" :data="item"  />
    <h1>Образование</h1>
    <Education v-for="item in data" :key="item.id" :data="item" />
    <h1>Деятельность</h1>
    <WorkExperience v-for="item in data" :key="item.id" :data="item"/>
    <Contacts />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import data from './data.json';
import Header from './components/Header.vue';
import About from './components/About.vue';
import Education from './components/Education.vue';
import WorkExperience from './components/WorkExperience.vue';
import Contacts from './components/Contacts.vue';

export default defineComponent({
  name: 'App',
  components: {
    Header,
    About,
    Education,
    WorkExperience,
    Contacts
  },
  data() {
    return {
      data: data,
    };
  },
  
});
</script>

<style lang="scss">
  body {
    margin: 0;
    background-color: rgba(211, 211, 211, 0.1);
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    section {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
      gap: 20px;
      padding: 0 30px;
      transform: translateY(-1000%);
      animation: slideIn 1.8s forwards;
    }
  }

  h1 {
    margin: 0;
    padding-top: 20px;
  }

  @keyframes slideIn {
    to {
      transform: translateY(0);
    }
  }

  .container {
    box-shadow: 0 0 15px 0 rgba(0, 0, 0, 0.473);
    padding: 20px;
    border-radius: 15px;
  }

</style>
