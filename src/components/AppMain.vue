<template>
   <main class="ms_container">
      <AppCard />
   </main>
</template>

<script>
import AppCard from './AppCard.vue';
export default {
   components: {
      AppCard,
   },
};
</script>

<style lang="scss" scoped>
.ms_container {
   max-width: 1000px;
   margin: 0 auto;
}
</style>
