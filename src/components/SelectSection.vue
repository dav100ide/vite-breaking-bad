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
         // in base al valore del select, stampo in pagino le card giuste
      },
   },
};
</script>

<style lang="scss" scoped></style>
