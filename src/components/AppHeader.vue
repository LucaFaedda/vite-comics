<script>
  export default {
      name: 'AppHeader',
      data(){
        return{
          listaHeader: [
            {
              nome: 'characters',
              status: false,
              url: '#'
            },
            {
              nome: 'comics',
              status: true,
              url: '#'
            },{
              nome: 'movies',
              status: false,
              url: '#'
            },
            {
              nome: 'tv',
              status: false,
              url: '#'
            },
            {
              nome: 'games',
              status: false,
              url: '#'
            },
            {
              nome: 'collectibles',
              status: false,
              url: '#'
            },
            {
              nome: 'videos',
              status: false,
              url: '#'
            },
            {
              nome: 'fans',
              status: false,
              url: '#'
            },
            {
              nome: 'news',
              status: false,
              url: '#'
            },
            {
              nome: 'shop',
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
      <div class="row">
        <div class="col-4">
          <img src="../assets/img/dc-logo.png" alt="logo-primario">

        </div>
        <div class="col-6">

        </div>
      </div>

    </div>
  </header>
</template>
<style lang="scss">
  @use '../styles/partials/variabiles' as *;
  header{
    margin: $margin2rem;
    .col-4{
      width: 40%;
    }
    .col-6{
      width: 60%;
    }
  }
</style>
