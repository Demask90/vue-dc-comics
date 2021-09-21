<template>
  <div >
      <div class="jumbo">

      </div>
  </div>
</template>

<script>

export default {
  name: 'Jumbotron',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .jumbo {
        background-image: url('../assets/img/jumbotron.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: top;
        width: 100%;
        height: 400px;
        margin-bottom: 10px;
    }
</style>
