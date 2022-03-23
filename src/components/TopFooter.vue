<template>
  <div class="cards">
    <img class="img-foot" :src="elementImg" :alt="elementText">
    <a :href="elementHref">
      <span class="foot-text">{{ elementText }}</span>
    </a>
  </div>
</template>

<script>
export default {
  name: 'TopFooter',
  props: {
    elementImg: String,
    elementText: String
  }
}
</script>

<style scoped lang="scss">
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
</style>
