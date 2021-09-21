<template>
  <main >

    <Jumbotron/>

    <div class="file_products w-60 flex top wrap">
      <div id="current_series">CURRENT SERIES</div>
      <ProductCard v-for="(product,index) in products" 
      :key="index"
      :prod="product"
      />
    </div>

    <button id="load_more">LOAD MORE</button>

  </main>
</template>

<script>
import Jumbotron from "@/components/Jumbotron.vue"
import ProductCard from "@/components/ProductCard.vue"
import ProdItems from "@/assets/data/dc-comics.json"
export default {
  name: 'Products',
  components: {
    ProductCard,
    Jumbotron
  },
  data() {
    return {
      products: ProdItems
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  main {
    width: 100%;
    background-color: #212121;
    color: white;
    padding-bottom: 50px;

    .file_products {
      position: relative;

      #current_series {
        position: absolute;
        top: -30px;
        background-color: #0C7CEC;
        padding: 10px;
        font-weight: bold;
      }
    }

    #load_more {
      position: absolute;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: #0C7CEC;
      padding: 10px 30px;
      font-weight: bold;
      border: none;
      color: white;
    }
  }
</style>
