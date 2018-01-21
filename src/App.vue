<template lang="pug">
  #app
    .box
      .comment#comment0 ほげほげほげほげほげほげ
      .comment#comment1 ほげほげほげほげほげほげ
      .comment#comment2 ほげほげほげほげほげほげ
      .comment#comment3 ほげほげほげほげほげほげ
      .comment#comment4 ほげほげほげほげほげほげ
      .comment#comment5 ほげほげほげほげほげほげ
      .comment#comment6 ほげほげほげほげほげほげ
      .comment#comment7 ほげほげほげほげほげほげ
      .comment#comment8 ほげほげほげほげほげほげ
      .comment#comment9 ほげほげほげほげほげほげ
      .comment#comment10 ほげほげほげほげほげほげ
      .comment#comment11 ほげほげほげほげほげほげ
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
    @for $i from 0 through 11 {
      #comment#{$i} {
        top: $i * 50px;
      }
    }
    #comment0 {
      animation-delay: 3s;
    }
    #comment1 {
      animation-delay: 7s;
    }
    #comment2 {
      animation-delay: 2s;
    }
    #comment3 {
      animation-delay: 5s;
    }
    #comment4 {
      animation-delay: 4s;
    }
    #comment5 {
      animation-delay: 9s;
    }
    #comment6 {
      animation-delay: 1s;
    }
    #comment7 {
      animation-delay: 6s;
    }
    #comment8 {
      animation-delay: 3s;
    }
    #comment9 {
      animation-delay: 5s;
    }
    #comment10 {
      animation-delay: 7s;
    }
    #comment11 {
      animation-delay: 2s;
    }
  }
</style>
