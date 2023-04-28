<script>
  import products from '../data/dc-comics.json';
  import card from './partial/card.vue';
  export default {
    name: 'Main',

    components: {
      card
    },

    data() {
      return {
        products
      }
    }
  }
</script>








<template>
  <main>
    <div class="jumbotron">
      <img src="" alt="">
    </div>

    <div class="container">
      <card
        v-for="(product, index) in products"
        :key="index"
        :thumb="product.thumb"
        :type="product.type"
        :series="product.series"
      />
    </div>
  </main>
</template>








<style lang="scss" scoped>
  @use '../scss/general/mixin' as *;

  main {
    background-color: black;
    color: white;
    
    .container {
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>