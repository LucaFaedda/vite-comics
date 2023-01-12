<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import AppSocial from './components/AppSocial.vue'
  export default {
      components:{
        AppHeader,
        AppContent,
        AppMain,
        AppFooter,
        AppSocial
      }
  }
</script>
<template >
  <div>
    <AppHeader></AppHeader>
    <AppContent></AppContent>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
    <AppSocial></AppSocial>
  </div>
</template>
<style lang="scss" >
// lo scoped non va in App.vue
  @use './styles/generals.scss' as*;
</style>
