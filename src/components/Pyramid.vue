<script>

export default {
  name: 'Pyramid',
  props: {
    level1: Number,
    level2: Number,
    level2_1: Number,
    level2_2: Number,
    level2_3: Number,
    level2_4: Number,
    level2_5: Number,
    level3: Number,
    level3_1: Number,
    level3_2: Number,
    level3_3: Number,
    level4: Number,
    level4_1: Number,
    level4_2: Number,
    level4_3: Number,
    level4_4: Number,
    level5: Number,
    level5_1: Number,
    level5_2: Number,
    level5_3: Number,
    level5_4: Number,
    level5_5: Number
  },
  methods: {
    calcTotalLevel1 () {
      return this.level1
    },
    calcTotalLevel2 () {
      let sum2 = this.level2 + this.level2_1 + this.level2_2 + this.level2_3 + this.level2_4 + this.level2_5
      sum2 = sum2 / 5
      return sum2
    },
    calcTotalLevel3 () {
      let sum3 = this.level3 + this.level3_1 + this.level3_2 + this.level3_3
      sum3 = sum3 / 5
      return sum3
    },
    calcTotalLevel4 () {
      let sum4 = this.level4 + this.level4_1 + this.level4_2 + this.level4_3 + this.level4_4
      sum4 = sum4 / 5
      return sum4
    },
    calcTotalLevel5 () {
      let sum5 = this.level4 + this.level5_1 + this.level5_2 + this.level5_3 + this.level5_4 + this.level5_5
      sum5 = sum5 / 5
      return sum5
    }
  }
}
</script>

<template>
  <div class="container-pyramid">
    <div class="pyramid">
        <div :class="this.level1 > 50 ? 'level': 'level shakey'" id="pyramid-level-1" v-on:click="calcTotalLevel1()">
            <div class="inside-text">
                {{ calcTotalLevel1() }}
            </div>
        </div>
        <div :class="calcTotalLevel2() > 50 ? 'level': 'level shakey'" id="pyramid-level-2">
            <div class="inside-text">
            {{ calcTotalLevel2() }}
            </div>
        </div>
        <div :class="calcTotalLevel3() > 50 ? 'level': 'level shakey'" id="pyramid-level-3">
            <div class="inside-text">
            {{ calcTotalLevel3() }}
            </div>
        </div>
        <div :class="calcTotalLevel4() > 50 ? 'level': 'level shakey'" id="pyramid-level-4">
            <div class="inside-text">
            {{ calcTotalLevel4() }}
            </div>
        </div>
        <div :class="this.level5 > 50 ? 'level': 'level shakey'" id="pyramid-level-5">
            <div class="inside-text">
            {{ calcTotalLevel5() }}
            </div>
        </div>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container-pyramid{
    max-width: 530px;
    margin:auto;
}
.shakey {
    animation: shake 0.5s;
    animation-iteration-count: infinite;
}

@keyframes shake {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}

.level {
    margin:10px;
    .inside-text{
        color: white;
        margin-left: -8px;
        padding-top: 24px;
        font-size: 14px;
        font-weight: bold;
    }
}

#pyramid-level-1 {
    border-bottom: 50px solid blue;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    height: 0;
    width: 0px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-2 {
    border-bottom: 50px solid green;
    border-left: 25px solid transparent;
    border-right: 25px solid transparent;
    height: 0;
    width: 50px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-3 {
  position: relative;
    border-bottom: 50px solid red;
    border-left: 23px solid transparent;
    border-right: 23px solid transparent;
    height: 0;
    width: 100px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-4 {
  position: relative;
    border-bottom: 60px solid purple;
    border-left: 28px solid transparent;
    border-right: 28px solid transparent;
    height: 0;
    width: 149px;
    margin-right:auto;
    margin-left:auto;
}

#pyramid-level-5 {
  position: relative;
    border-bottom: 60px solid orange;
    border-left: 30px solid transparent;
    border-right: 30px solid transparent;
    height: 0;
    width: 223px;
    margin-right:auto;
    margin-left:auto;
}

</style>
