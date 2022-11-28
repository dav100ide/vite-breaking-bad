<template>
   <div class="ms_card">
      <img :src="characterInfo.img" :alt="characterInfo.name" class="img-fluid" />
      <h3>{{ characterInfo.name }}</h3>
      <div class="series">Breaking Bad</div>
      <div class="status">{{ characterInfo.status }}</div>
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
   background-color: steelblue;
}
</style>
