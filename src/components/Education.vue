<template>
  <div class="container" v-if="data.id === 'Education'">
    <div class="container__title">
      <h2>{{ data.title }}</h2>
      <button @click="toggleData" :class="{ expanded: dataExpanded }">
        {{ dataExpanded ? 'Свернуть' : 'Развернуть' }}
      </button>
    </div>

    <div class="container__data" :class="{ expanded: dataExpanded, 'flex-row': data.title === 'Rubius-Academy' }" :style="{ opacity: aboutOpacity }">
      <p>{{ data.description }}</p>
      <a :href="data.image" target="_blank">
        <img :src="data.image" alt="">
      </a>
    </div>
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
    data() {
      return {
        dataExpanded: false,
        aboutOpacity: 1,
      };
    },
    methods: {
      toggleData() {
        this.dataExpanded = !this.dataExpanded;
      },
    },
  });
</script>
  
  
<style lang="scss" scoped>
  .container {
    width: 50%;
    &__title {
      display: flex;
      align-items: center;
      justify-content: space-between;
      align-items: center;

      h2 {
        margin: 0;
        width: 60%;

        @media (max-width: 550px) {
          font-size: 16px;
        }
      }
    }

    &__data {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0 auto;
      max-height: 0;
      overflow: hidden;
      transition: max-height 1.7s ease;

      &.flex-row {
        display: flex;
        flex-direction: row;

        a {
          width: 350%;
          img {
            margin-top: 10px;

            height: 100%;
            border-radius: 5px;
          }
          @media (max-width: 1250px) {
          width: 100%;
        }
      }

        @media (max-width: 1250px) {
          flex-direction: column;
        }

      }

      a {
        img {
          margin-top: 10px;
          width: 100%;
          height: 100%;
          border-radius: 5px;
        }
      }

      &.expanded {
        max-height: 150vh;
      }

      @media (max-width: 1250px) {
        flex-direction: column;
        display: flex;
        align-items: center;
        width: 100%;
      }
    }

    button {
        border: none;
        background-color: none;
        color: rgb(53, 31, 250);
        background: none;
        font-size: medium;
        cursor: pointer;
        border-radius: 8px;
        width: 40%;

        &:hover {
          background: rgb(53, 31, 250);
          color: white;
          transition: .7s;
          border-radius: 8px;
        }
    }

    @media (max-width: 1250px) {
      min-width: 100%;
    }
  }
</style>