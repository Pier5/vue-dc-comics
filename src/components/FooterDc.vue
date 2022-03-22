<template>
  <footer>
    <div class="top-footer">
      <div class="cards" v-for="(element, index) in arrBuy" :key="index">
          <img class="img-foot" :src="element.img" :alt="element.text">
          <a :href="element.href"><span class="foot-text">{{ element.text }}</span></a>
      </div>
    </div>
    <div class="middle-footer">
      <img class="main-img-foot" src="../assets/img/footer-bg.jpg" alt="">
    </div>
    <div class="bottom-footer">
      <div class="container">
        <div class="sign-up"><a href="#"><span class="text-sign">Sign-up now!</span></a></div>
        <div class="social-text">Follow us</div>
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
    margin: 0 60px;
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
    height: 350px;
  .main-img-foot {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
.bottom-footer {
  background-color: #303030;
  padding: 20px 0;
  .sign-up {
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
