<script>
  import Header from './components/Header.vue';
  import Main from './components/Main.vue';
  import Shop from './components/Shop.vue';
  import Footer from './components/Footer.vue';

  export default {
    name: 'App',
    components: {
      Header,
      Main,
      Shop,
      Footer
    },
    data() {
      return {
      }
    }
  }
</script>

<template>
  <Header/>
  <Main/>
  <Shop/>
  <Footer/>
</template>

<style lang="scss">
  @import './scss/main.scss';
</style>