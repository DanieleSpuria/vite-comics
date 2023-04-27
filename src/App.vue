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
  <div class="container">
    <Header/>
    <Main/>
    <Shop/>
    <Footer/>
  </div>
</template>

<style lang="scss" scoped>
  @import './scss/main.scss';
</style>