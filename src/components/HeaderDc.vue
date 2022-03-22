<template>
  <header>
    <div class="container">
      <img class="img-logo" src="../assets/img/dc-logo.png" alt="logo DC">
      <ul>
        <li v-for="(link, index) in links" :key="index"><a href="link.href">{{ link.link }}</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderDc',
  data () {
    return {
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
  }
}
</script>

<style scoped lang="scss">
  .img-logo {
    width: 5%;
    margin-right: auto;
  }
  li {
  display: inline-block;
  a {
    text-decoration: none;
    color: black;
    padding: 1rem;
  }
}
</style>
