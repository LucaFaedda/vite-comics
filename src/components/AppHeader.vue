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
        activeItem(index)
        {
          this.listaHeader[index].stato = !this.listaHeader[index].stato
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
              <a :href="item.url" :class="item.stato ? 'active' : ''" @click="activeItem(index)">{{ item.nome }}</a>
            </li>
          </ul>

        </div>
      </nav>

    </div>
  </header>
</template>
<style lang="scss" scoped >
  @use '../styles/partials/variabiles' as *;
  @use '../styles/partials/mixins' as *;
  header{
    margin: $margin2rem;
    height: 100px;
    .row{
      @include d-flex-center;
      width: 100%;
      justify-content: space-between;
      height: 100%;

      .col-4{
        width: 20%;
      }
      .col-6{
        width: 80%;
        display: flex;
        justify-content: flex-end;
        height: 100%;
        ul{
          @include d-flex;
          height: 100%;
          li{
            height: 100%;
            a{
            margin: 0rem 5px;
            height: 100%;
              &.active, &:hover{
                color: $primarycolor;
              }
              &.active{
              padding-bottom: 64px;
              border-bottom: 5px solid;
              border-spacing: 10px;
            }
            
          } 
          }
        }
      }
    }
  }

</style>
