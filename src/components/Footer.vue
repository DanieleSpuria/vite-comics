<script>
  import {dcComics, footerShop, dC, sites, social} from '../data/db'
  export default { 
    name: 'Footer',
    data() {
      return {
        dcComics,
        footerShop, 
        dC,
        sites, 
        social
      }
    }
  }
</script>








<template>
  <footer>
    
    <div class="top">
      <div class="container">
        <div class="left">
          <div class="col">
            <h3>DC COMICS</h3>
            <nav>
              <ul>
                <li
                  v-for="(link, index) of dcComics"   
                  :key="index"
                >
                  {{ link.name }}
                </li>
              </ul>
            </nav>

            <h3>SHOP</h3>
            <nav>
              <ul>
                <li
                  v-for="(link, index) of footerShop"   
                  :key="index"
                >
                  {{ link.name }}
                </li>
              </ul>
            </nav>
          </div>

          <div class="col">
            <h3>DC</h3>
            <nav>
              <ul>
                <li
                  v-for="(link, index) of dC"   
                  :key="index"
                >
                  {{ link.name }}
                </li>
              </ul>
            </nav>
          </div>

          <div class="col">
            <h3>SITES</h3>
            <nav>
              <ul>
                <li
                  v-for="(link, index) of sites"   
                  :key="index"
                >
                  {{ link.name }}
                </li>
              </ul>
            </nav>
          </div>
        </div>

        <div class="right">
          <img src="../assets/img/dc-logo-bg.png" alt="DC">
        </div>
      </div>
    </div>

    <div class="bottom">
      <div class="container">
        <button>
          <h3>SIGN-UP NOW!</h3>
        </button>

        <div class="social">
          <h3>FOLLOW US</h3>
          <div
            class="circle"
            v-for="(link, index) of social"   
            :key="index"
          >
            <img
              :src="link"
              alt="social"
            >
          </div>
        </div>
      </div>
    </div>
    
  </footer>
</template>







<style lang="scss" scoped>
  @use '../scss/partials/mixin' as *;
  @use '../scss/partials/variables' as *;

  footer {
    height: 600px;
    .top {
      height: 80%;
      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      overflow: hidden;

      .container {
        display: flex;

        .left {
          display: flex;
          width: 40%;
          margin: 20px 0;
  
          .col {
            margin-right: 30px;

            li {
              font-size: 13px;
              padding: 4px 0;;
              color: #959595;
            }
          }
        }
  
        .right{
          display: flex;
          justify-content: end;
          position: relative;
          width: 60%;
  
          img {
            position: absolute;
            top: -80px;
            width: 80%;
          }
        }
      }
    }

    .bottom {
      height: 20%;
      background-color: #303030;

      .container {
        height: 100%;
        @include flex('vertical');
        justify-content: space-between;

        button {
          padding: 0 10px;
          background-color: #303030;
          border: 1px solid $primary-color;
        }

        .social {
          @include flex;

          h3 {
            margin: 0 10px;
            color: $primary-color;
          }
          .circle {
            margin: 0 10px;
            cursor: pointer;
          }
        }
      }
    }
  }
</style>