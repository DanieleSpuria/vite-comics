<script>
  export default {
    name: 'Main'
  }
</script>

<template>
  <main>
    MAIN
  </main>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/mixin' as *;

  main {
    width: 100%;
    height: 200px;
    background-color: black;
    color: white;
    @include flex;
  }
</style>