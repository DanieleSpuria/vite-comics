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

    mounted() {
      console.log(this.products);
    }
  }
</script>

<template>
  <main>
    <h1>{{ name }}</h1>
  </main>
</template>

<style lang="scss" scoped>
  @use '../scss/general/mixin' as *;

  main {
    width: 100%;
    height: 200px;
    background-color: black;
    color: white;
    @include flex;
  }
</style>