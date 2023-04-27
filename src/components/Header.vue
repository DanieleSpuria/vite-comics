<script>
  import {menu} from '../data/db';
  export default {
    name: 'Header',
    data() {
      return {
        menu
      }
    }
  }
</script>









<template>
  <header>
    <div class="container">
      <img src="src/assets/img/dc-logo.png" alt="logo">
      <nav>
        <ul>
          <li
            v-for="(link, index) of menu"   
            :key="index"
          >
            <a
              href="link.href"
              :class="{'active' : link.active}"
            > {{ link.name }} </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>








<style lang="scss" scoped>
  @use '../scss/partials/mixin' as *;
  @use '../scss/partials/variables' as *;

  header {
    width: 100%;
    height: 100px;
    border-bottom: 1px solid black;

    .container {
      @include flex('vertical');
      justify-content: space-between;
      height: 100%;

      img {
        width: 80px
      }

      nav {
        height: 100%;
  
        ul {
          height: 100%;
          @include flex;
  
          li {
            height: 100%;
            padding: 0 15px;
            font-size: 12px;
            text-transform: uppercase;

            a {
              @include flex;
              height: 100%;
              color: black;
              &.active {
                border-bottom: 5px solid $primary-color;
              }

              &:hover {
              color: $primary-color;
            }
            }
          }
        }
      } 
    }
  }
</style>