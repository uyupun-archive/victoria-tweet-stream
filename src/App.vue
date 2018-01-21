<template>
  <div id="app">
    <div class="box">
      <div v-bind:class="className"></div>
      <div id="comment0" class="comment" v-bind:class="[ color[0], delay[0] ]">ほげほげほげほげほげほげ</div>
      <div id="comment1" class="comment" v-bind:class="[ color[1], delay[1] ]">ほげほげほげほげほげほげ</div>
      <div id="comment2" class="comment" v-bind:class="[ color[2], delay[2] ]">ほげほげほげほげほげほげ</div>
      <div id="comment3" class="comment" v-bind:class="[ color[3], delay[3] ]">ほげほげほげほげほげほげ</div>
      <div id="comment4" class="comment" v-bind:class="[ color[4], delay[4] ]">ほげほげほげほげほげほげ</div>
      <div id="comment5" class="comment" v-bind:class="[ color[5], delay[5] ]">ほげほげほげほげほげほげ</div>
      <div id="comment6" class="comment" v-bind:class="[ color[6], delay[6] ]">ほげほげほげほげほげほげ</div>
      <div id="comment7" class="comment" v-bind:class="[ color[7], delay[7] ]">ほげほげほげほげほげほげ</div>
      <div id="comment8" class="comment" v-bind:class="[ color[8], delay[8] ]">ほげほげほげほげほげほげ</div>
      <div id="comment9" class="comment" v-bind:class="[ color[9], delay[9] ]">ほげほげほげほげほげほげ</div>
      <div id="comment10" class="comment" v-bind:class="[ color[10], delay[10] ]">ほげほげほげほげほげほげ</div>
      <div id="comment11" class="comment" v-bind:class="[ color[11], delay[11] ]">ほげほげほげほげほげほげ</div>
      <div id="comment12" class="comment" v-bind:class="[ color[12], delay[12] ]">ほげほげほげほげほげほげ</div>
      <div id="comment13" class="comment" v-bind:class="[ color[13], delay[13] ]">ほげほげほげほげほげほげ</div>
      <div id="comment14" class="comment" v-bind:class="[ color[14], delay[14] ]">ほげほげほげほげほげほげ</div>
      <div id="comment15" class="comment" v-bind:class="[ color[15], delay[15] ]">ほげほげほげほげほげほげ</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      className: 'white',
      color: [
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
      delay: [
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0',
        'delay0'
      ],
      colorPalette: [
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
      ],
      delayPalette: [
        'delay0',
        'delay1',
        'delay2',
        'delay3',
        'delay4',
        'delay5',
        'delay6',
        'delay7',
        'delay8',
        'delay9',
        'delay10',
        'delay11',
        'delay12',
        'delay13',
        'delay14',
        'delay15',
        'delay16',
        'delay17',
        'delay18',
        'delay19',
        'delay20',
        'delay21',
        'delay22',
        'delay23',
        'delay24',
        'delay25',
      ]
    }
  },
  methods: {
    changeDelay() {
      let delayNum = Math.floor(Math.random() * 16)
      for (let i = 0; i <= 15; i++) {
        delayNum = Math.floor(Math.random() * 16)
        this.delay[i] = this.delayPalette[delayNum]
      }
    },
    changeColor() {
      let colorNum = Math.floor(Math.random() * 10)
      this.className = this.colorPalette[colorNum]
      for (let i = 0; i <= 15; i++) {
        colorNum = Math.floor(Math.random() * 10)
        this.color[i] = this.colorPalette[colorNum]
      }
    }
  },
  created() {
    this.changeColor()
    this.changeDelay()
    setInterval(() => {
      this.changeColor()
      this.changeDelay()
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
  }
  .delay0 {
    animation-delay: 0s;
  }
  .delay1 {
    animation-delay: 1s;
  }
  .delay2 {
    animation-delay: 2s;
  }
  .delay3 {
    animation-delay: 3s;
  }
  .delay4 {
    animation-delay: 4s;
  }
  .delay5 {
    animation-delay: 5s;
  }
  .delay6 {
    animation-delay: 6s;
  }
  .delay7 {
    animation-delay: 7s;
  }
  .delay8 {
    animation-delay: 8s;
  }
  .delay9 {
    animation-delay: 9s;
  }
  .delay10 {
    animation-delay: 10s;
  }
  .delay11 {
    animation-delay: 11s;
  }
  .delay12 {
    animation-delay: 12s;
  }
  .delay13 {
    animation-delay: 13s;
  }
  .delay14 {
    animation-delay: 14s;
  }
  .delay15 {
    animation-delay: 15s;
  }
  /*.delay16 {*/
    /*animation-delay: 16s;*/
  /*}*/
  /*.delay17 {*/
    /*animation-delay: 17s;*/
  /*}*/
  /*.delay18 {*/
    /*animation-delay: 18s;*/
  /*}*/
  /*.delay19 {*/
    /*animation-delay: 19s;*/
  /*}*/
  /*.delay20 {*/
    /*animation-delay: 20s;*/
  /*}*/
  /*.delay21 {*/
    /*animation-delay: 21s;*/
  /*}*/
  /*.delay22 {*/
    /*animation-delay: 22s;*/
  /*}*/
  /*.delay23 {*/
    /*animation-delay: 23s;*/
  /*}*/
  /*.delay24 {*/
    /*animation-delay: 24s;*/
  /*}*/
  /*.delay25 {*/
    /*animation-delay: 25s;*/
  /*}*/
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
