<script>
  import products from '../data/dc-comics.json';
  import card from './partial/card.vue';
  export default {
    name: 'Main',
    components: {
      card,
    },
    props: {
      name: String,
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
    <!-- <h1>{{ name }}</h1> -->
    <div class="jumbotron">
      <img src="" alt="">
    </div>

    <div class="container">
      <card
        :thumb="products[0].thumb"
        :type="products[0].type"
        :series="products[0].series"
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