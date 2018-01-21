<template>
  <div id="app">
    <div class="box">
      <div v-bind:class="className"></div>
      <div id="comment0" class="comment" v-bind:class="target[0]">ほげほげほげほげほげほげ</div>
      <div id="comment1" class="comment" v-bind:class="target[1]">ほげほげほげほげほげほげ</div>
      <div id="comment2" class="comment" v-bind:class="target[2]">ほげほげほげほげほげほげ</div>
      <div id="comment3" class="comment" v-bind:class="target[3]">ほげほげほげほげほげほげ</div>
      <div id="comment4" class="comment" v-bind:class="target[4]">ほげほげほげほげほげほげ</div>
      <div id="comment5" class="comment" v-bind:class="target[5]">ほげほげほげほげほげほげ</div>
      <div id="comment6" class="comment" v-bind:class="target[6]">ほげほげほげほげほげほげ</div>
      <div id="comment7" class="comment" v-bind:class="target[7]">ほげほげほげほげほげほげ</div>
      <div id="comment8" class="comment" v-bind:class="target[8]">ほげほげほげほげほげほげ</div>
      <div id="comment9" class="comment" v-bind:class="target[9]">ほげほげほげほげほげほげ</div>
      <div id="comment10" class="comment" v-bind:class="target[10]">ほげほげほげほげほげほげ</div>
      <div id="comment11" class="comment" v-bind:class="target[11]">ほげほげほげほげほげほげ</div>
      <div id="comment12" class="comment" v-bind:class="target[12]">ほげほげほげほげほげほげ</div>
      <div id="comment13" class="comment" v-bind:class="target[13]">ほげほげほげほげほげほげ</div>
      <div id="comment14" class="comment" v-bind:class="target[14]">ほげほげほげほげほげほげ</div>
      <div id="comment15" class="comment" v-bind:class="target[15]">ほげほげほげほげほげほげ</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      className: 'white',
      target: [
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white',
        'white'
      ],
      color: [
        'white',
        'red',
        'pink',
        'orange',
        'yellow',
        'green',
        'light-blue',
        'blue',
        'purple',
        'black'
      ]
    }
  },
  methods: {
    changeColor() {
      let colorNum = Math.floor(Math.random() * 10)
      this.className = this.color[colorNum]
      for (let i = 0; i <= 15; i++) {
        colorNum = Math.floor(Math.random() * 10)
        this.target[i] = this.color[colorNum]
        console.log(this.target[i])
      }
    }
  },
  created() {
    setInterval(() => {
      this.changeColor()
    }, 25000)
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
    @for $i from 0 through 15 {
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
    #comment11 {
      animation-delay: 2s;
    }
    #comment12 {
      animation-delay: 2s;
    }
    #comment13 {
      animation-delay: 2s;
    }
    #comment14 {
      animation-delay: 2s;
    }
    #comment15 {
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
