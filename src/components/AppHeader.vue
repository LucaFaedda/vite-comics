<script>
  export default {
      name: 'AppHeader',
      data(){
        return{
          itemActive: 0,
          listaHeader: [
            {
              nome: 'CHARACTERS',
              stato: false,
              url: '#'
            },
            {
              nome: 'COMICS',
              stato: true,
              url: '#'
            },{
              nome: 'MOVIES',
              stato: false,
              url: '#'
            },
            {
              nome: 'TV',
              stato: false,
              url: '#'
            },
            {
              nome: 'GAMES',
              stato: false,
              url: '#'
            },
            {
              nome: 'COLLECTIBLES',
              stato: false,
              url: '#'
            },
            {
              nome: 'VIDEOS',
              stato: false,
              url: '#'
            },
            {
              nome: 'FANS',
              stato: false,
              url: '#'
            },
            {
              nome: 'NEWS',
              stato: false,
              url: '#'
            },
            {
              nome: 'SHOP',
              stato: false,
              url: '#'
            },
  
          ]

        }
      },
      methods: {
        activeItem()
        {
          if(stato == false){
            stato == true
          }
          else{
            stato == false
          }
        }
      },
  }
</script>
<template >
  <header>
    <div class="container">
      <nav class="row">
        <div class="col-4">
          <img src="../assets/img/dc-logo.png" alt="logo-primario">

        </div>
        <div class="col-6">
          <ul>
            <li v-for="(item, index) in listaHeader" :key="index">
              <a :href="item.url" :class="item.stato ? 'active' : ''" @click="activeItem()">{{ item.nome }}</a>
            </li>
          </ul>

        </div>
      </nav>

    </div>
  </header>
</template>
<style lang="scss" >
  @use '../styles/partials/variabiles' as *;
  @use '../styles/partials/mixins' as *;
  header{
    margin: $margin2rem;
    height: 100px;
    .row{
      @include d-flex;
      width: 100%;
      align-items: center;
      justify-content: space-between;

      .col-4{
        width: 20%;
      }
      .col-6{
        width: 80%;
        display: flex;
        justify-content: flex-end;
        ul{
          @include d-flex;
          li a{
            margin: 0rem 5px;
              &.active, &:hover{
                color: #0282f9;
              }
              &.active{
              padding-bottom: 20px;
              border-bottom: 3px solid;
              border-spacing: 10px;
            }
          }
        }
      }
    }
  }

</style>
