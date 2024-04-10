<template>
  <HeaderC/>
  <MainC/>
  <FooterC/>
</template>

<script>
import HeaderC from './components/HeaderC.vue';
import MainC from './components/MainC.vue';
import FooterC from './components/FooterC.vue';
 
export default {
    name: 'App',
    components: {
        HeaderC,
        MainC,
        FooterC,
    }
  }
</script>

<style lang="scss" scoped>

</style>
