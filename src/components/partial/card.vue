<script>
  export default {
    name: 'Card',
    props: {
      thumb: String,
      type: String,
      series: String
    }
  }
</script>
  
<template>
  <div class="box">
    <div class="card">
      <img :src="thumb" :alt="type">
      <span>{{ series }}</span>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  .box {
    margin-top: 20px;
    padding: 20px;
    width: calc(100% / 6);
    text-align: center;

    &:hover {
      transform: scale(1.2);
      animation-name: rotate;
      animation-duration: .5s;
    }

    @keyframes rotate {
      0% {transform: rotate(0deg) scale(1)}
      100% {transform: rotate(360deg) scale(1.2)}
    }
 }
</style>