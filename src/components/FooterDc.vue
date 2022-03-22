<template>
  <footer>
    <div class="top-footer">
      <div class="cards" v-for="(element, index) in arrBuy" :key="index">
            <img class="img-foot" :src="element.img" :alt="element.text">
           <a :href="element.href"><span class="foot-text">{{ element.text }}</span></a>
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
</style>
