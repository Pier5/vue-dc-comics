<template>
  <div id="app">
    <HeaderDc />
    <MainDc />
    <CardsDcNovels />
    <FooterDc />
  </div>
</template>

<script>
import HeaderDc from './components/HeaderDc.vue'
import MainDc from './components/MainDc.vue'
import CardsDcNovels from './components/CardsDcNovels.vue'
import FooterDc from './components/FooterDc.vue'
export default {
  name: 'App',
  components: {
    HeaderDc,
    MainDc,
    FooterDc,
    CardsDcNovels
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss';
</style>
