<template>
    <div class="container" v-if="data.id === 'AboutMe'">
        <img :src="data.image" alt="">

        <p>{{ data.description }}</p>
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
        display: flex;
        align-items: center;
        gap: 70px;
        margin-top: 70px;
        max-width: 70%;

        @media (max-width: 1250px) {
            flex-direction: column;
            justify-content: flex-start;
            gap: 0;
            min-width: 100%;

        }

        img {
            max-width: 50%;
            height: auto;
            border-radius: 15px;

            @media (max-width: 1250px) {
              max-width: 80vw;
            }
        }



    }
</style>
