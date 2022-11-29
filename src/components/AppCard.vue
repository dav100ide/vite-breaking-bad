<template>
   <div>
      <div class="ms_card p-3 text-center">
         <img :src="characterInfo.img" :alt="characterInfo.name" class="img-fluid" />
         <h3>{{ characterInfo.name }}</h3>
         <div class="series">{{ characterInfo.category }}</div>
         <div class="status">{{ characterInfo.status }}</div>
      </div>
   </div>
</template>

<script>
export default {
   props: {
      characterInfo: Object,
   },
};
</script>

<style lang="scss" scoped>
.ms_card {
   background-color: var(--primary-color);
   .series,
   .status {
      color: var(--neutral-color-200);
   }
}
</style>
