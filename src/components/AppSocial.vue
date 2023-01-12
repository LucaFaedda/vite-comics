<script>
  export default {
    name: 'AppSocial',
    data(){
        return{
            arraySocial:[
                {
                    img: '../src/assets/img/footer-facebook.png',
                    href:'#'
                },
                {
                    img: '../src/assets/img/footer-twitter.png',
                    href:'#'
                },
                {
                    img: '../src/assets/img/footer-youtube.png',
                    href:'#'
                },
                {
                    img: '../src/assets/img/footer-pinterest.png',
                    href:'#'
                },
                {
                    img: '../src/assets/img/footer-periscope.png',
                    href:'#'
                },

            ]
        }
    }
  }
</script>
<template >
  <div class="bk-grey">
    <div class="container">
        <div class="row">
            <div class="pulsanti">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="lista-social">
                <ul>
                    <li><h2>Follows us</h2></li>
                    <li v-for="(item, index) in arraySocial" :key="index">
                        <a :href="item.href">
                            <img :src="item.img">
                        </a>
                    </li>
                </ul>
                
            </div>
        </div>

    </div>
    
  </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .bk-grey{
        background-color: #303030;
        position: relative;
        .row{
            @include d-flex;
            width: $width100;
            justify-content: space-between;
            align-items: center;
            .pulsanti{
                width: $width50;
                margin: 4rem 0rem;
                display: flex;
                button{
                    padding: 15px;
                    border: 1px solid #0282f9;
                    background-color: transparent;
                    color: $colorwhite;
                    font-size: 25px;
                }
            }
            .lista-social{
                ul{
                    @include d-flex;
                    li:first-child{
                        color:#0282f9;
                    }
                    li{
                        margin:0.5rem;
                    }
                }
            }
            
        }

    }
    
</style>
