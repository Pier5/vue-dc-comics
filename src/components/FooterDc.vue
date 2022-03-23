<template>
  <footer>
    <div class="top-footer">
      <div class="cards" v-for="(element, index) in arrBuy" :key="index">
          <img class="img-foot" :src="element.img" :alt="element.text">
          <a :href="element.href"><span class="foot-text">{{ element.text }}</span></a>
      </div>
    </div>
    <div class="middle-footer">
      <div class="container">
        <div class="col-left">
        <div class="col_col-left">
          <ul>
              <li class="li-title">Dc Comics</li>
              <li class="li-footer" v-for="(link, index) in arrDcComics" :key="index"><a :href="link.href">{{ link.text }}</a></li>
          </ul>
          <ul>
              <li class="li-title">Shop</li>
              <li class="li-footer" v-for="(link, index) in arrShop" :key="index"><a :href="link.href">{{ link.text }}</a></li>
          </ul>
        </div>
        <div class="col_col-middle">
          <ul>
              <li class="li-title">Dc</li>
              <li class="li-footer" v-for="(link, index) in arrDc" :key="index"><a :href="link.href">{{ link.text }}</a></li>
          </ul>
        </div>
        <div class="col_col-right">
          <ul>
              <li class="li-title">Sites</li>
              <li class="li-footer" v-for="(link, index) in arrSites" :key="index"><a :href="link.href">{{ link.text }}</a></li>
          </ul>
        </div>
      </div>
      <div class="col-right">
        <img class="img-jumbo" src="../assets/img/dc-logo-bg.png" alt="logo dc">
      </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="container">
        <button class="sign-up"><a href="#"><span class="text-sign">Sign-up now!</span></a></button>
        <h3 class="social-text">Follow us</h3>
        <a v-for="(element,index) in arrSocial" :key="index" class="social-img" :href="element.href">
          <img :src="element.img" :alt="element.text">
        </a>
      </div>
    </div>
  </footer>
</template>

<script>
import dcComics from '../assets/img/buy-comics-digital-comics.png'
import dcMerch from '../assets/img/buy-comics-merchandise.png'
import dcShop from '../assets/img/buy-comics-shop-locator.png'
import dcSubs from '../assets/img/buy-comics-subscriptions.png'
import dcPower from '../assets/img/buy-dc-power-visa.svg'
import fb from '../assets/img/footer-facebook.png'
import twitter from '../assets/img/footer-twitter.png'
import yt from '../assets/img/footer-youtube.png'
import pinterest from '../assets/img/footer-pinterest.png'
import periscope from '../assets/img/footer-periscope.png'
export default {
  name: 'FooterDc',
  data () {
    return {
      arrBuy: [
        {
          href: '#',
          img: dcComics,
          text: 'digital comics'
        },
        {
          href: '#',
          img: dcMerch,
          text: 'dc-merchandise'
        },
        {
          href: '#',
          img: dcSubs,
          text: 'subscrition'
        },
        {
          href: '#',
          img: dcShop,
          text: 'comic shop locator'
        },
        {
          href: '#',
          img: dcPower,
          text: 'dc power visa'
        }
      ],
      arrDcComics: [
        {
          href: '#',
          text: 'Characters'
        },
        {
          href: '#',
          text: 'Comics'
        },
        {
          href: '#',
          text: 'Movies'
        },
        {
          href: '#',
          text: 'Tv'
        },
        {
          href: '#',
          text: 'Games'
        },
        {
          href: '#',
          text: 'Videos'
        },
        {
          href: '#',
          text: 'News'
        }
      ],
      arrShop: [
        {
          href: '#',
          text: 'Shop DC'
        },
        {
          href: '#',
          text: 'Shop DC Collectibles'
        }
      ],
      arrDc: [
        {
          href: '#',
          text: 'Terms Of Use'
        },
        {
          href: '#',
          text: 'Privacy policy (New)'
        },
        {
          href: '#',
          text: 'Ad Choices'
        },
        {
          href: '#',
          text: 'Advertising'
        },
        {
          href: '#',
          text: 'Jobs'
        },
        {
          href: '#',
          text: 'Subscriptions'
        },
        {
          href: '#',
          text: 'Talent Workshops'
        },
        {
          href: '#',
          text: 'CPSC Certificates'
        },
        {
          href: '#',
          text: 'Ratings'
        },
        {
          href: '#',
          text: 'Shop Help'
        },
        {
          href: '#',
          text: 'Contact Us'
        }
      ],
      arrSites: [
        {
          href: '#',
          text: 'DC'
        },
        {
          href: '#',
          text: 'MAD Magazine'
        },
        {
          href: '#',
          text: 'DC Kids'
        },
        {
          href: '#',
          text: 'DC Univers'
        },
        {
          href: '#',
          text: 'DC Power Visa'
        }
      ],
      arrSocial: [
        {
          href: '#',
          img: fb,
          text: 'facebook'
        },
        {
          href: '#',
          img: twitter,
          text: 'twitter'
        },
        {
          href: '#',
          img: yt,
          text: 'youtube'
        },
        {
          href: '#',
          img: pinterest,
          text: 'pinterest'
        },
        {
          href: '#',
          img: periscope,
          text: 'periscope'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables";
.top-footer {
  background-color: $blue-color;
  padding: 40px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  .cards {
    display: flex;
    align-items: center;
    margin: 0 50px;
    .img-foot {
      width: 35px;
      margin-right: 8px;
    }
    a {
      text-decoration: none;
      .foot-text {
        font-size: .9rem;
        text-transform: uppercase;
        color: white;
      }
    }
  }
}
.middle-footer {
    width: 100%;
    height: 380px;
    background-image: url(../assets/img/footer-bg.jpg);
    display: flex;
    overflow-y: hidden;
    .col-left {
      width: 50%;
      display: flex;
      a {
          color: lightgrey;
          text-decoration: none;
          font-size: .8rem;
        }
        .li-title {
          color: white;
          text-transform: uppercase;
          font-weight: bolder;
          margin: 15px 0;
        }
        .li-footer {
          padding: .2rem 0;
        }
      .col_col-left,
      .col_col-middle,
      .col_col-right {
        padding: 20px 0;
        margin-right: 3rem;
      }
      ul {
        list-style: none;
      }
    }
    .col-right {
      width: 50%;
      display: flex;
      justify-content: flex-end;
      .img-jumbo {
        width: 80%;
      }
    }
}
.bottom-footer {
  background-color: #303030;
  padding: 20px 0;
  .sign-up {
    background-color: transparent;
    border: 3px solid $blue-color;
    padding: 10px;
    a {
      text-decoration: none;
    }
    .text-sign {
      font-size: 1rem;
      text-transform: uppercase;
      font-weight: bolder;
      color: white;
    }
  }
  .social-text {
    margin-left: auto;
    margin-right: 20px;
    color: $blue-color;
    text-transform: uppercase;
    font-weight: bolder;
    font-size: 1.2rem;
  }
  .social-img {
    margin: 0 10px;
  }
}
</style>
