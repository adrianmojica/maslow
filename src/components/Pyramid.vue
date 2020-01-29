<script>

export default {
  name: 'Pyramid',
  props: {
    level1: Number,
    level2: Number,
    level3: Number,
    level4: Number,
    level5: Number
  },
  methods: {
    calcTotalLevel1 () {
      return this.level1
    },
    calcTotalLevel2 () {
      return this.level1
    },
    calcTotalLevel3 () {
      return this.level1
    },
    calcTotalLevel4 () {
      return this.level1
    },
    calcTotalLevel5 () {
      return this.level1
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
        <div :class="this.level2 > 50 ? 'level': 'level shakey'" id="pyramid-level-2">
            <div class="inside-text">
            {{ this.level2 }}
            </div>
        </div>
        <div :class="this.level3 > 50 ? 'level': 'level shakey'" id="pyramid-level-3">
            <div class="inside-text">
            {{ this.level3 }}
            </div>
        </div>
        <div :class="this.level4 > 50 ? 'level': 'level shakey'" id="pyramid-level-4">
            <div class="inside-text">
            {{ this.level4 }}
            </div>
        </div>
        <div :class="this.level5 > 50 ? 'level': 'level shakey'" id="pyramid-level-5">
            <div class="inside-text">
            {{ this.level5 }}
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
