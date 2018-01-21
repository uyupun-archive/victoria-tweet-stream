<template lang="pug">
  #app
    .box
      .comment#comment1 ほげほげほげほげほげほげ
      .comment#comment2 ほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげほげ
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
    position: relative;
    .comment {
      position: absolute;
      right: 0;
      font-size: 32px;
      white-space: nowrap;
      color: white;
      text-shadow:
        black 0.7px 0.7px 0, black -0.7px -0.7px 0,/*右下、左上*/
        black -0.7px 0.7px 0, black 0.7px -0.7px 0,/*右上、左下*/
        black 0 0.7px 0, black  -0.7px 0,/*右、左*/
        black -0.7px 0 0, black 0.7px 0 0;/*上、下*/
      animation-name: comments;
      animation-duration: 25s;
      animation-iteration-count: infinite;
      animation-fill-mode: both;
      animation-timing-function: linear;
    }
    @keyframes comments {
      from {
        transform: translate(101%, 0);
      }
      to {
        transform: translate(-4500px, 0);
      }
    }
  }
</style>
