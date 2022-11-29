<template>
   <div class="ms_container text-center mb-2">
      <label class="me-2" for="series">scegli categoria</label>
      <select class="p-1 rounded-3" name="series" id="series" @change="changeCategory">
         <option value="bb-better-call">breaking bad and better call</option>
         <option value="breaking-bad">Breaking Bad</option>
         <option value="better-call">Better Call Saul</option>
      </select>
   </div>
</template>

<script>
import { store } from '../store.js';
import axios from 'axios';
export default {
   data() {
      return {
         store,
      };
   },
   methods: {
      changeCategory() {
         // prendo il select nel dom
         const option = document.getElementById('series').value;
         //
         if (option === 'breaking-bad') {
            axios.get('https://www.breakingbadapi.com/api/characters?category=Breaking+Bad').then((response) => {
               this.store.charactersInfo = response.data;
            });
         } else if (option === 'better-call') {
            axios.get('https://www.breakingbadapi.com/api/characters?category=Better+Call+Saul').then((response) => {
               this.store.charactersInfo = response.data;
            });
         } else if (option === 'bb-better-call') {
            axios
               .get('https://www.breakingbadapi.com/api/characters') //
               .then((response) => {
                  this.store.charactersInfo = response.data;
               });
         }
      },
   },
};
</script>

<style lang="scss" scoped></style>
