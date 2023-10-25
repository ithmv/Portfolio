<template>
    <div class="container"  v-if="data.id === 'WorkExperience'">
      <p>{{data.date}}</p>
      <section>
        <h4>{{data.title}}</h4>
        <p>{{data.description}}</p>
    </section>
    </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    props: {
      data: {
        type: Object,
        required: true,
      },
    },
  });
</script>

<style scoped lang="scss">
  .container {
    text-align: center;
    width: 70% ;
    display: flex;
    justify-content: space-between;
    align-items: center;

    @media (max-width: 1250px) {
        width: 100%;
      }

    p {
      margin: 0;
      @media (max-width: 550px) {
        font-size: 12px;
      }
    }

    section {
      display: flex;
      flex-direction: column;
      width: 70%;
      h4 {
        margin: 0;
      }
    }
  }
</style>

