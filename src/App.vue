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
    border: solid 5px #000;
    margin: auto;
    width: auto;
    height: 400px;
    overflow: hidden;
    .comment {
      font-size: 120%;
      animation-name: comments;
      animation-duration: 10s;
      animation-timing-function: linear;
      animation-iteration-count: 1;
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
