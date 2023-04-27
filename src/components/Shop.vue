<script>
  import {shop} from '../data/db'
  export default {
    name: 'Shop',
    data() {
      return {
        shop
      }
    }
  }
</script>








<template>
  <div class="shop">
    <div class="container">
      <nav>
        <ul>
          <li
              v-for="(link, index) of shop"   
              :key="index"
            >
              <img :src="link.img" alt="imgShop">
              <a :href="link.href">{{ link.name }}</a>
            </li>
        </ul>
      </nav>
    </div>
  </div>
</template>








<style lang="scss" scoped>
  @use '../scss/partials/variables'  as *;
  @use '../scss/partials/mixin'  as *;

  .shop {
    width: 100%;
    height: 150px;
    background-color: $primary-color;
    @include flex;

    ul {
      @include flex('vertical');
      justify-content: space-around;
      color: white;

      li {
        @include flex('vertical');
        transition: all .3s;

        &:hover {
          transform:scale(1.2)
        } 

        img {
          width: 50px;
          margin-right: 10px;
        }

        a {
          text-transform: capitalize;
          color: white;
        }
      }
    }
  }
</style>