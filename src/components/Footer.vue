<script>
  import {footerShop, dC, sites} from '../data/db'
  export default { 
    name: 'Footer',
    data() {
      return {
        footerShop, 
        dC,
        sites
      }
    }
  }
</script>

<template>
  <footer>
    
    <div class="top">
      <div class="container">
        <div class="left">

        </div>

        <div class="right">
          <img src="../assets/img/dc-logo-bg.png" alt="DC">
        </div>
      </div>
    </div>

    <div class="bottom">

    </div>
    
  </footer>
</template>

<style lang="scss" scoped>
  footer {
    height: 600px;
    .top {
      height: 80%;
      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      overflow: hidden;

      .right{
        position: relative;
        width: 60%;

        img {
          position: absolute;
          top: -50px;
          width: 60%;
        }
      }
    }

    .bottom {
      height: 20%;
      background-color: #303030;
    }
  }
</style>