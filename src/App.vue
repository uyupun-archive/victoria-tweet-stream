<template lang="pug">
  div#app
    h1 sample
    .box
      .comment ほげ
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style lang="scss">
  h1 {
    color: red;
  }

  .box {
    .comment {
      font-size: 150%;
      color: white;
      text-shadow:
          black 0.5px 0.5px 0, black -0.5px -0.5px 0,/*右下、左上*/
          black -0.5px 0.5px 0, black 0.5px -0.5px 0,/*右上、左下*/
          black 0px 0.5px 0, black  -0.5px 0,/*右、左*/
          black -0.5px 0 0, black 0.5px 0 0;/*上、下*/
      animation-name: comments;
      animation-duration: 10s;
      animation-timing-function: linear;
      animation-iteration-count: 1;
      animation-fill-mode: both;
    }

    @keyframes comments {
      from{
        transform: translate(110%, 0);
      }
      to{
        transform: translate(-100%, 0);
      }
    }
  }
</style>
