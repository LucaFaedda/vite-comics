<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
  export default {
      components:{
        AppHeader,
        AppContent,
        AppMain,
        AppFooter
      }
  }
</script>
<template >
  <div>
    <AppHeader></AppHeader>
    <AppContent></AppContent>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss">
  @use './styles/generals.scss' as*;
</style>
