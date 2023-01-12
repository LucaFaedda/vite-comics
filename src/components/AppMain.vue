<script>
    export default {
        name: 'AppMain',
        data(){
            return{
                iconsArray:[
                    {
                        nome: 'DIGITAL COMICS',
                        href: '#',
                        img: '../src/assets/img/buy-comics-digital-comics.png'
                    },
                    {
                        nome: 'DC MERCHANDASIE',
                        href: '#',
                        img: '../src/assets/img/buy-comics-merchandise.png'
                    },
                    {
                        nome: 'SUBSCRIPTION',
                        href: '#',
                        img: '../src/assets/img/buy-comics-subscriptions.png'
                    },
                    {
                        nome: 'COMIC SHOP LOCATION',
                        href: '#',
                        img: '../src/assets/img/buy-comics-shop-locator.png'
                    },
                    {
                        nome: 'DC POWER VISA',
                        href: '#',
                        img: '../src/assets/img/buy-dc-power-visa.svg'
                    },
                ] // nelle img andava src??? 
            }

        },

    }
</script>
<template lang="">
    <div class="icons">
        <div class="container">
            <ul>
                <li v-for="(item, index) in iconsArray" :key="index">
                <img :src="item.img">
                <a :href="item.href">{{item.nome}}</a>
                </li>
            </ul>      
        </div>
    </div>
    
</template>
<style lang="scss">
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .icons{
        @include d-flex;
        justify-content: space-around;
        background-color: #0282f9;
        position: relative;
        .container{
            ul{
                @include d-flex;
                align-items: center;
                margin: $margin4rem;
                li{
                    @include d-flex;
                    align-items:center;
                    margin-right: 20px;
                    img{
                        width: 2.5rem;
                        margin: 0px 10px;
                        &:hover{
                            filter: invert(100);
                        }
                    }
                    a{
                        font-size: 14px;
                        color: $colorwhite;
                        &:hover{
                            color:#000
                        }
                    }
                }
            }
        }
    }
</style>