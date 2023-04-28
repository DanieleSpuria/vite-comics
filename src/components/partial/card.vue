<script>
  export default {
    name: 'Card',

    props: {
      thumb: String,
      type: String,
      series: String,
      price: String
    }
  }
</script>
  







<template>
  <div class="box">
    <div class="card">
      <img :src="thumb" :alt="type">
      <span>{{ series }}</span>
      <div class="circle">{{ price }}</div>
    </div>
  </div>
</template>









<style lang="scss" scoped>
  @use '../../scss/general/variables' as *;
  @use '../../scss/general/mixin' as *;

  .box {
    margin-top: 20px;
    padding: 20px;
    width: calc(100% / 6);
    text-align: center;

    &:hover {
      transform: scale(1.2);
      animation-name: rotate;
      animation-duration: .3s;
    }

    &:hover .card .circle {
      opacity: 1;
    }

    @keyframes rotate {
      0% {transform: rotate(0deg) scale(1)}
      100% {transform: rotate(360deg) scale(1.2)}
    }

    .card {
      position: relative;
      height: 100%;

      img {
        height: 90%;
      }

      .circle {
        position: absolute;
        top: -25px;
        right:-25px;
        width: 60px;
        aspect-ratio: 1/1;
        border-radius: 50%;
        padding: 10px;
        background-color: $primary-color;
        opacity: 0;
        @include flex;
      }
    }
  }
</style>