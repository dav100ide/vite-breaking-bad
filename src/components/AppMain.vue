<template>
   <main class="ms_container p-3">
      <ResultBar />
      <div class="row g-3">
         <AppCard class="col-6 col-md-4 col-lg-3" v-for="character in store.charactersInfo" :characterInfo="character" />
      </div>
   </main>
</template>

<script>
import axios from 'axios';
import AppCard from './AppCard.vue';
import ResultBar from './ResultBar.vue';
import { store } from '../store.js';

export default {
   components: {
      AppCard,
      ResultBar,
   },

   data() {
      return {
         store,
      };
   },
   created() {
      axios
         .get('https://www.breakingbadapi.com/api/characters') //
         .then((response) => {
            this.store.charactersInfo = response.data;
         });
   },
};
</script>

<style lang="scss" scoped>
.ms_container {
   background-color: var(--neutral-color-100);
}
</style>
