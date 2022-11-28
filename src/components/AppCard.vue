<template>
   <div>card</div>
</template>

<script>
export default {
   data() {
      return {
         characters: [],
      };
   },
   created() {
      axios
         .get('https://www.breakingbadapi.com/api/characters') //
         .then((response) => {
            console.log(response);
         });
   },
};
</script>

<style lang="scss" scoped></style>
