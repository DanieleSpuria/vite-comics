<script>
  import products from '../data/dc-comics.json';
  export default {
    name: 'Main',
    props: {
      name: String,
    },

    data() {
      return {
        products,
      }
    },

    mounted () {
      console.log();
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
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
      <div class="box">
        <div class="card">
          <img :src="products[0].thumb" alt="">
          <span>{{ products[0].series }}</span>
        </div>
      </div>
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

      .box {
        margin-top: 20px;
        padding: 20px;
        width: calc(100% / 6);
        text-align: center;

        &:hover {
          transform: scale(1.2);
          animation-name: rotate;
          animation-duration: .5s;
        }

        @keyframes rotate {
          0% {transform: rotate(0deg) scale(1)}
          100% {transform: rotate(360deg) scale(1.2)}
        }
      }
    }
  }
</style>