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
      ]
      }
    }
  }
</script>
<template>
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
</template>
<style lang="scss" >
    @use '../styles/partials/variabiles' as *;
    @use '../styles/partials/mixins' as *;
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
    
</style>
