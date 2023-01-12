<script>
  export default {
    name: 'AppContent'
  }
</script>
<template lang="">
  <div class="content">
    <div class="jumbo">

    </div>
    <div class="container">
       

    </div>
    
  </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .content{
        @include d-flex-center;
        justify-content: center;
        flex-direction: row;
        .jumbo{
            height: 280px;
            width: 100%;
            background-image: url("../assets/img/jumbotron.jpg");
            background-size: cover;
        }
    }

</style>
