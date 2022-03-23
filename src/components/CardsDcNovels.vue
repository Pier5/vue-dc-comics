<template>
  <div class="cards">
    <img :src="cardImg" :alt="cardSeries">
    <h2>{{ cardSeries }}</h2>
  </div>
</template>

<script>
export default {
  name: 'CardsDcNovels',
  props: {
    cardImg: String,
    cardSeries: String
  }
}
</script>

<style scoped lang="scss">
  .cards {
    width: calc(100% / 6 - 20px);
    margin: 15px 10px;
    img {
      height: 200px;
      width: 100%;
    }
    h2 {
      color: white;
      font-size: 1.2rem;
    }
  }
</style>
