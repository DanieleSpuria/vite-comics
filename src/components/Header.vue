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
            {{ link.name }}
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
        @include flex;
  
        ul {
        @include flex;
  
          li {
            padding: 15px;
            font-size: 12px;
            text-transform: uppercase;

            &:hover {
              color: $primary-color;
            }
          }
        }
      } 
    }
  }
</style>