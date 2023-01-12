<script>
  export default {
    name: 'AppFooter',
    data(){
      return{
        DcComicsArray: [
          {
            nome: 'Characters',
            href: '#',
            titolo: 'DC COMICS'
          },
          {
            nome: 'Comics',
            href: '#'
          },
          {
            nome: 'Movies',
            href: '#'
          },
          {
            nome: 'TV',
            href: '#'
          },
          {
            nome: 'Games',
            href: '#'
          },
          {
            nome: 'Videos',
            href: '#'
          },
          {
            nome: 'News',
            href: '#'
          },
        ],
        DcArray: [
          {
            nome: 'Terms Of Use',
            href: '#',
            titolo: 'DC '
          },
          {
            nome: 'Privacy policy(New)',
            href: '#'
          },
          {
            nome: 'Ad Choices',
            href: '#'
          },
          {
            nome: 'Advertising',
            href: '#'
          },
          {
            nome: 'Jobs',
            href: '#'
          },
          {
            nome: 'Subscriptions',
            href: '#'
          },
          {
            nome: 'Talent Workshops',
            href: '#'
          },
          {
            nome: 'CPSC Certificates',
            href: '#'
          },
          {
            nome: 'Ratings',
            href: '#'
          },
          {
            nome: 'Shop Help',
            href: '#'
          },
          {
            nome: 'Contact Us',
            href: '#'
          },
        ],
        SitesArray:[
        {
          nome: 'DC',
          href: '#',
          titolo: 'SITES'
        },
        {
          nome: 'MAD Magazine',
          href: '#'
        },
        {
          nome: 'DC Kids',
          href: '#'
        },
        {
          nome: 'DC Universe',
          href: '#'
        },
        {
          nome: 'DC Power Visa',
          href: '#'
        },
      ],
      ShopArray:[
        {
          nome: 'Shop DC',
          href: '#',
          titolo: 'SHOP'
        },
        {
          nome: 'Shop DC Collections',
          href: '#'
        },
      ],
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
                ],
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

            ] // nelle img andava src??? 
      }
    }
  }
</script>
<template>
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
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-4">
          <div>
            <ul>
              <li><h2>DC comics</h2></li>
              <li v-for="(item, index) in DcComicsArray" :key="index">
                <a :href="item.href">{{ item.nome }}</a>
              </li>
            </ul>
            <ul>
              <li><h2>Shop</h2></li>
              <li v-for="(item, index) in ShopArray" :key="index">
                <a :href="item.href">{{ item.nome }}</a>
              </li>
            </ul>
          </div>
          <div class="margin-2rem">
            <ul>
              <li><h2>DC</h2></li>
              <li v-for="(item, index) in DcArray" :key="index">
                <a :href="item.href">{{ item.nome }}</a>
              </li>
            </ul>
          </div>
          <div>
            <ul>
              <li><h2>Sites</h2></li>
              <li v-for="(item, index) in SitesArray" :key="index">
                <a :href="item.href">{{ item.nome }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-6">
          <img src="../assets/img/dc-logo-bg.png" alt="dc-logo">
        </div>
      </div>
      <div class="fine">

      </div>

    </div>
        
  </footer>
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
<style lang="scss" scoped >
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
    .icons{
        @include d-flex;
        justify-content: space-around;
        background-color:$primarycolor;
        position: relative;
        .container{
            ul{
                @include d-flex-center;
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
    footer{
      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      padding: 3rem 0rem;
      .row{
        @include d-flex;
        width: $width100;
        .col-4{
          width: 40%;
          @include d-flex;
            li{
              margin:10px 5px;
              h2{
                color:$colorwhite;
                margin-bottom: 1rem;
              }
              a{
                color: #959595;
                font-size: 14px;
              }
            }
            .margin-2rem{
              margin:0rem 2rem;
            }
        }
        .col-6{
          display: flex;
          flex-direction: row-reverse;
          width: 60%;
          img{
            width: 30%;
            position: absolute;
            bottom: 0px;
            
          }
        }
      }
    }
    .bk-grey{
        background-color: #303030;
        position: relative;
        .row{
            @include d-flex-center;
            width: $width100;
            justify-content: space-between;
            .pulsanti{
                width: $width50;
                margin: 2rem 0rem;
                display: flex;
                button{
                    padding: 15px;
                    border: 1px solid $primarycolor;
                    background-color: transparent;
                    color: $colorwhite;
                    font-size: 25px;
                    cursor: pointer;
                    &:hover{
                        color: #303030;
                        background-color: $primarycolor;
                        border: 1px solid#303030;
                    }
                }
            }
            .lista-social{
                ul{
                    @include d-flex;
                    li:first-child{
                        color:$primarycolor;
                    }
                    li{
                        margin:0.5rem;
                    }
                }
            }
            
        }

    }
    
</style>
