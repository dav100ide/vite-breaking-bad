<template>
   <main class="ms_container row">
      <AppCard class="col-6 col-md-4 col-lg-3" v-for="character in charactersInfo" :characterInfo="character" />
   </main>
</template>

<script>
import AppCard from './AppCard.vue';
import axios from 'axios';

export default {
   components: {
      AppCard,
   },

   data() {
      return {
         charactersInfo: [],
      };
   },
   created() {
      axios
         .get('https://www.breakingbadapi.com/api/characters') //
         .then((response) => {
            this.charactersInfo = response.data;
            console.log(response.data[2]);
         });
   },
};
</script>

<style lang="scss" scoped>
.ms_container {
   max-width: 1100px;
   margin: 0 auto;
}
</style>
