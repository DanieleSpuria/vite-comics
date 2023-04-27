<script>
  import menu from '../data/db';
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
    <img src="" alt="logo">
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
  </header>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/mixin.scss' as *;

  header {
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid black;

    nav {
      @include flex;

      ul {
      @include flex
      }
    } 
  }
</style>