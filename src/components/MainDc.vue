<template>
  <main>
    <div class=" container main-container">
    <span class="main-text">
      --> Content goes here
    </span>
  </div>
  </main>
</template>

<script>
export default {
  name: 'MainDc'
}
</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables";
main {
  background-color: black;
  .main-container {
    padding: 40px 0;
    .main-text {
    color: white;
    text-transform: uppercase;
    font-weight: bolder;
    font-size: 1.1rem;
  }
  }
}
</style>
