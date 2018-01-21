<template>
  <div id="app">
    <div class="box">
      <div id="comment0" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment1" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment2" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment3" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment4" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment5" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment6" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment7" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment8" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment9" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment10" class="comment">ほげほげほげほげほげほげ</div>
      <div id="comment11" class="comment">ほげほげほげほげほげほげ</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {

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
  .white {
    color: #fff;
  }
  .red {
    color: #ea3423;
  }
  .pink {
    color: #ef8784;
  }
  .orange {
    color: #f6c243;
  }
  .yellow {
    color: #fefe54;
  }
  .green {
    color: #75fb4c;
  }
  .light-blue {
    color: #75fbfd;
  }
  .blue {
    color: #1c00f5;
  }
  .purple {
    color: #b024f6;
  }
  .black {
    color: #000;
  }
</style>
