<script>
  import CardDc from './CardDc.vue'
  export default {
    CardDc,
    name: 'AppContent',
    data(){
      return{

      }
    }
  }
</script>
<template lang="">
  <div class="content">
    <div class="jumbo">

    </div>
    <div class="bk-black">
      <div class="container">
         <CardDc></CardDc>
  
      </div>
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
            height: 400px;
            width: 100%;
            background-image: url("../assets/img/jumbotron.jpg");
            background-size: cover;
        }
        .bk-black{
          background-color: #1c1c1c;
        }
    }

</style>
