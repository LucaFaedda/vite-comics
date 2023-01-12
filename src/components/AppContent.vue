<script>
  export default {
    name: 'AppContent'
  }
</script>
<template lang="">
  <div class="content">
    <div class="container">
        <h2 class="text-center">
      Content goes here 
        </h2>

    </div>
    
  </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .content{
        height: 100px;
        background-color: #1c1c1c;
        @include d-flex;
        justify-content: center;
        align-items: center;
        flex-direction: row;

        .text-center{
            color: #fff;
        }
    }

</style>
