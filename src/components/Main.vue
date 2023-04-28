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
      <img src="../assets/img/jumbotron.jpg" alt="jumbo">
    </div>

    
    <div class="container">
      <div class="title">
        <h4>CURRENT SERIES</h4>
      </div>

      <div class="row">
        <card
        v-for="(product, index) in products"
        :key="index"
        :thumb="product.thumb"
        :type="product.type"
        :series="product.series"
        :price="product.price"
        />
      </div>

      <div class="more">
        <h5>LOAD MORE</h5>
      </div>
    </div>
  </main>
</template>








<style lang="scss" scoped>
  @use '../scss/general/mixin' as *;
  @use '../scss/general/variables' as *;

  main {
    background-color: #1c1c1c;
    color: white;
    
    .jumbotron {
      img {
        height: 400px;
        object-fit: cover;
        object-position: top 
      }
    }

    .container {
      position: relative;
      padding: 25px;
      @include flex;
      flex-direction: column;

      .title,
      .more {
        width: 170px;
        padding: 5px 10px;
        background-color: $primary-color;
        font-size: 14px;
        text-align: center;
      }

      .title {
        position: absolute;
        top: -15px;
        left: 0;
      }

      .more {
        margin-top: 25px;
        cursor: pointer;
      }

      .row {
      display: flex;
      flex-wrap: wrap;
      }
    }
  }
</style>