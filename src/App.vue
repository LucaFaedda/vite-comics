<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
  export default {
      components:{
        AppHeader,
        AppMain,
        AppFooter
      }
  }
</script>
<template >
  <div>
    <AppHeader></AppHeader>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss' as*;
</style>
