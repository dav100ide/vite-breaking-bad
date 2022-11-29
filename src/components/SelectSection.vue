<template>
   <div class="ms_container text-center mb-2">
      <label class="me-2" for="series">scegli categoria</label>
      <select class="p-1 rounded-3" name="series" id="series" @change="changeCategory">
         <option value="ashdoia" selected>selezionaa</option>
         <option value="breaking-bad">Breaking Bad</option>
         <option value="bb-better-call">Breaking Bad, Better Call Saul</option>
         <option value="better-call">Better Call Saul</option>
      </select>
   </div>
</template>

<script>
import { store } from '../store.js';
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
         // in base al valore del select, stampo in pagino le card giuste
         // if (option === 'breaking-bad') {
         //    const filteredArr = store.charactersInfo.filter((characterInfo) => {
         //       characterInfo.category === 'Breaking Bad';
         //       this.store.charactersInfo = filteredArr;
         //       console.log(characterInfo.category);
         //    });
         // } else if (option === 'bb-better-call') {
         //    const filteredArr = store.charactersInfo.filter((characterInfo) => {
         //       characterInfo.category === 'Breaking Bad, Better Call Saul';
         //       this.store.charactersInfo = filteredArr;
         //    });
         // } else if (option === 'better-call') {
         //    const filteredArr = store.charactersInfo.filter((characterInfo) => {
         //       characterInfo.category === 'Better Call Saul';
         //       this.store.charactersInfo = filteredArr;
         //    });
         // }
      },
   },
};
</script>

<style lang="scss" scoped></style>
