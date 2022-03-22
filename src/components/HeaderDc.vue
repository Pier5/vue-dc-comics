<template>
  <header>
    <div class="container">
      <img class="img-logo" src="../assets/img/dc-logo.png" alt="logo DC">
      <ul>
        <li v-for="(link, index) in links" :key="index" @click="setActiveIndex(index)" :class="{active: index == activeIndex}"><a :href="link.href">{{ link.link }}</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderDc',
  data () {
    return {
      activeIndex: 0,
      links: [
        {
          href: '#',
          link: 'Characters'
        },
        {
          href: '#',
          link: 'Comics'
        },
        {
          href: '#',
          link: 'Movies'
        },
        {
          href: '#',
          link: 'Tv'
        },
        {
          href: '#',
          link: 'Games'
        },
        {
          href: '#',
          link: 'Collectibles'
        },
        {
          href: '#',
          link: 'Videos'
        },
        {
          href: '#',
          link: 'Fans'
        },
        {
          href: '#',
          link: 'News'
        },
        {
          href: '#',
          link: 'Shop'
        }
      ]
    }
  },
  methods: {
    setActiveIndex (index) {
      this.activeIndex = index
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables";
header {
  padding: 20px 0;
}
.img-logo {
  width: 5%;
  margin-right: auto;
}
li {
  display: inline-block;
  &.active a {
    color: $heavenly-color;
    border-bottom: 5px solid $heavenly-color;
  }
  a {
    text-decoration: none;
    color: black;
    padding: 1rem;
    text-transform: uppercase;
    font-weight: bolder;
    font-size: .8rem;
  }
}
</style>
