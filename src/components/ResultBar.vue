<template>
   <div class="my-2 p-2 fw-bold">Ci sono {{ store.charactersInfo.length }} personaggi</div>
</template>

<script>
import { store } from '../store.js';
export default {
   data() {
      return {
         store,
      };
   },
};
</script>

<style lang="scss" scoped>
div {
   background-color: var(--primary-color-400);
}
</style>
