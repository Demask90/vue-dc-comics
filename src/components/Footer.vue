<template>
  <footer>

    <div id="footer_top">
      <ul class="flex center middle w-60">
        <li class="icons flex middle center" v-for="(icon, index) in icons" :key="index"> 
            <img :src="require(`../assets/img/${icon.img}`)" alt="icon.text">
            <h3>{{ icon.text.toUpperCase() }}</h3>
        </li>
      </ul>
    </div>
    
    
    <div id="footer_bottom">
      <div class="w-60 flex middle">
        <div id="left_bottom" class="flex">
          <div class="flex-col">

            <ul class="list-link">
              <span class="title-list">DC COMICS</span>
              <li v-for="(link, index) in footDCComics" :key="index"><a href="">{{link.text}}</a></li>
            </ul>

            <ul class="list-link">
              <span class="title-list">SHOP</span>
              <li v-for="(link, index) in footShop" :key="index"><a href="">{{link.text}}</a></li>
            </ul>

          </div>


          <div class="flex">

            <ul class="list-link">
              <span class="title-list">DC</span>
              <li v-for="(link, index) in footDC" :key="index"><a href="">{{link.text}}</a></li>
            </ul>

            <ul class="list-link">
              <span class="title-list">SITES</span>
                <li v-for="(link, index) in footSites" :key="index"><a href="">{{link.text}}</a></li>
            </ul>

          </div>

        </div>
      
        <div id="right_bottom">
          <img src="../assets/img/dc-logo-bg.png" alt="logo DC">
        </div>
      </div>
      
      <div class="banner_footer flex middle">

        <div class="w-60 flex between middle">

          <div class="sign-up">
              <button> SIGN-UP NOW!</button>
          </div>

          <div class="socials flex middle">
              <span class="follow">FOLLOW US</span>
              <div v-for="(social, index) in socialsLink" :key="index" class="img-social">
                  <a :href="social.url"><img :src="require(`../assets/${social.icon}`)" :alt="social.name"></a>
              </div>
          </div>

        </div>

      </div>
      

    </div>
  </footer>
</template>

<script>
import Links from '@/assets/data/Links.js'
import Socials from '@/assets/data/Socials.js'

export default {
  name: 'Footer',

  data() {
    return {
      footDCComics : Links.footDCComics,
      footShop : Links.footShop,
      footDC : Links.footDC,
      footSites : Links.footSites,
      socialsLink: Socials,
      icons: [
        {   
            img: 'buy-comics-digital-comics.png',
            text: 'Digital Comics'
        },
        {   
            img: 'buy-comics-merchandise.png',
            text: 'DC Merchandise'
        },
        {   
            img: 'buy-comics-subscriptions.png',
            text: 'Subscriptions'
        },
        {   
            img: 'buy-comics-shop-locator.png',
            text: 'Shop Locator'
        },
        {   
            img: 'buy-dc-power-visa.svg',
            text: 'Power Visa'
        },
    ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/vars";

#footer_top {
  width: 100%;
  background-color: $primary;

  .icons {
    width: calc(100% / 5);
    padding: 40px 0;

    img {
      width: 15%;
    }

    h3 {
      color: white;
      padding: 10px;
      font-size: 0.9em;
    }
  }
}

#footer_bottom {
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  color: white;

  #left_bottom {
    width: 100%;

    .list-link {
      margin: 0 10px;
      color: white;

      .title-list {
        margin: 5px;
      }

      li {
          list-style: none;
          
          color: white;

          a {
            color: grey;
            font-size: 0.9em;
            text-decoration-line: none;
          }
        }
    }
    
  }
  
  #right_bottom {
    img {
      width: 100%;
      object-fit: cover;

    }
  }
}
    
.banner_footer{
    width: 100%; 
    height: 100px; 
    background-color: #303030;

        button{
            border: 2px solid $primary;
            background-color: transparent;
            padding: 15px 25px;
            color: white;
            font-size: 0.9em;
            cursor: pointer;
            transition: 0.2s;

            &:hover{
                background-color: $primary;
                
            }
        }

        .follow {
            color: $primary;
            font-weight: bold;
            font-size: 0.8em;
        }

            .img-social{ 
                width: 40px;
                margin-left: 20px;
                transition: 0.3s;

                img{
                    width: 100%;
                    
                }

                &:hover{
                    filter: brightness(1.3);
                }
            }
        }
        
</style>
