<template>
  <div>
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

<style>

</style>
