<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import SelectSection from './components/SelectSection.vue';

export default {
   components: {
      AppHeader,
      AppMain,
      SelectSection,
   },
};
</script>

<template>
   <AppHeader />
   <SelectSection />
   <AppMain />
</template>

<style lang="scss">
@import './style/global.scss';
</style>
