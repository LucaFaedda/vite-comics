<script>
  import CardDc from './CardDc.vue'
  import ArrayImageDc from '../assets/data/ArrayImageDc'
  export default {
    components:{
      CardDc,
    },
    name: 'AppContent',
    data(){
      return{
        comics: ArrayImageDc
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
        <div class="card-container">
          <CardDc v-for="(item, index) in comics" :key="index" :fumetto="item"></CardDc>
        </div>
        <div class="btn-content">
          <button class="btn-primary"><h4>Load More</h4></button>
        </div>
      </div>
    </div>
    
  </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .content{
        
        .jumbo{
            height: 400px;
            width: 100%;
            background-image: url("../assets/img/jumbotron.jpg");
            background-size: cover;
        }
        .bk-black{
          background-color: #1c1c1c;
          .card-container{
            display: flex;
            flex-wrap: wrap;
            padding: 2rem;
          }
          .btn-content{
            display: flex;
            justify-content: center;
            padding-bottom: 3rem;
            .btn-primary{
              padding: 10px 80px;
              color: $colorwhite;
              background-color: $primarycolor;
              border: 1px solid transparent;
              cursor: pointer;
              &:hover{
                background-color: #1c1c1c;
                border: 1px solid $primarycolor;
              }
            }
          }
        }
    }

</style>
