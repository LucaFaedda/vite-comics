<script>
  export default {
      name: 'AppHeader',
      data(){
        return{
          listaHeader: [
            {
              nome: 'CHARACTERS',
              status: false,
              url: '#'
            },
            {
              nome: 'COMICS',
              status: true,
              url: '#'
            },{
              nome: 'MOVIES',
              status: false,
              url: '#'
            },
            {
              nome: 'TV',
              status: false,
              url: '#'
            },
            {
              nome: 'GAMES',
              status: false,
              url: '#'
            },
            {
              nome: 'COLLECTIBLES',
              status: false,
              url: '#'
            },
            {
              nome: 'VIDEOS',
              status: false,
              url: '#'
            },
            {
              nome: 'FANS',
              status: false,
              url: '#'
            },
            {
              nome: 'NEWS',
              status: false,
              url: '#'
            },
            {
              nome: 'SHOP',
              status: false,
              url: '#'
            },
  
          ]

        }
      }
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
              <a :href="item.url" :class="item.status ? 'active' : ''">{{ item.nome }}</a>
            </li>
          </ul>

        </div>
      </nav>

    </div>
  </header>
</template>
<style lang="scss">
  @use '../styles/partials/variabiles' as *;
  @use '../styles/partials/mixins' as *;
  header{
    margin: $margin2rem;
    .row{
      @include d-flex;
      width: 100%;
      align-items: center;

      .col-4{
        width: 40%;
      }
      .col-6{
        width: 60%;

        ul{
          list-style: none;
          @include d-flex;
          li a{
            margin: 0rem 0.75rem;
            font-size: 20px;
            font-weight: 500;
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
