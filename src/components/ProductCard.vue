<template>
  <div class="product-card">
    <img :src="prod.thumb" :alt="prod.series">
    <div>{{prod.series.toUpperCase()}}</div>
  </div>
</template>

<script>

export default {
  name: 'Productcard',
  props: ['prod']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   .product-card {
    width: calc(100% / 6);
    height: 100%;
    padding: 20px 10px;

    img {
      width: 100%;
      height: 100%;
    }
    div {
      font-size: 0.8em;
    }
  }
</style>
