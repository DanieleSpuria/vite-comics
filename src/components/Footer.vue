<script>
  import {dcComics, footerShop, dC, sites} from '../data/db'
  export default { 
    name: 'Footer',
    data() {
      return {
        dcComics,
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

    </div>
    
  </footer>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/mixin' as *;

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
            width: 60%;
          }
        }
      }
    }

    .bottom {
      height: 20%;
      background-color: #303030;
    }
  }
</style>