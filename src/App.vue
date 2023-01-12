<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'
import CardDc from './components/CardDc.vue'
  export default {
      components:{
        AppHeader,
        AppContent,
        AppFooter,
        CardDc
      }
  }
</script>
<template >
  <div>
    <AppHeader></AppHeader>
    <AppContent></AppContent>
    <AppFooter></AppFooter>
  </div>
</template>
<style lang="scss" >
// lo scoped non va in App.vue
  @use './styles/generals.scss' as*;
</style>
