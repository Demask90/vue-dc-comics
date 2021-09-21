<template>
  <div id="app" class="w-80">
    <Header/>
    <Products/>
    <Footer/>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Products from './components/Products.vue'
import Footer from './components/Footer.vue'

export default { 
  name: 'App',
  components: {
    Header,
    Products,
    Footer
  }
}
</script>

<style lang="scss">
@import "./style/generals";
#app {
  width: 100%;
}
</style>
