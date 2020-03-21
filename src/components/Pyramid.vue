<script>

export default {
  name: 'Pyramid',
  props: {
    average1: Number,
    level1: Number,
    level2: Number,
    average2: Number,
    level2_1: Number,
    level2_2: Number,
    level2_3: Number,
    level2_4: Number,
    level2_5: Number,
    average3: Number,
    level3: Number,
    level3_1: Number,
    level3_2: Number,
    level3_3: Number,
    average4: Number,
    level4: Number,
    level4_1: Number,
    level4_2: Number,
    level4_3: Number,
    level4_4: Number,
    average5: Number,
    level5: Number,
    level5_1: Number,
    level5_2: Number,
    level5_3: Number,
    level5_4: Number,
    level5_5: Number
  },
  methods: {
    calcTotalLevel1 () {
      this.average1 = this.level1
      return this.level1
    },
    calcTotalLevel2 () {
      let sum2 = this.level2 + this.level2_1 + this.level2_2 + this.level2_3 + this.level2_4 + this.level2_5
      sum2 = sum2 / 5
      this.average2 = sum2
      return sum2
    },
    calcTotalLevel3 () {
      let sum3 = this.level3 + this.level3_1 + this.level3_2 + this.level3_3
      sum3 = sum3 / 5
      this.average3 = sum3
      return sum3
    },
    calcTotalLevel4 () {
      let sum4 = this.level4 + this.level4_1 + this.level4_2 + this.level4_3 + this.level4_4
      sum4 = sum4 / 5
      this.average4 = sum4
      return sum4
    },
    calcTotalLevel5 () {
      let sum5 = this.level4 + this.level5_1 + this.level5_2 + this.level5_3 + this.level5_4 + this.level5_5
      sum5 = sum5 / 5
      this.average5 = sum5
      return sum5
    }
  }
}
</script>

<template>
  <div class="container-pyramid">
    <div class="pyramid">
        <div :class="this.level1 > 70 ? 'level': 'level shakey'" id="pyramid-level-1" v-on:click="calcTotalLevel1()">
            <div class="inside-text">
                {{ calcTotalLevel1() }}
            </div>
        </div>
        <div :class="calcTotalLevel2() > 70 ? 'level': 'level shakey'" id="pyramid-level-2">
            <div class="inside-text">
            {{ calcTotalLevel2() }}
            </div>
        </div>
        <div :class="calcTotalLevel3() > 70 ? 'level': 'level shakey'" id="pyramid-level-3">
            <div class="inside-text">
            {{ calcTotalLevel3() }}
            </div>
        </div>
        <div :class="calcTotalLevel4() > 70 ? 'level': 'level shakey'" id="pyramid-level-4">
            <div class="inside-text">
            {{ calcTotalLevel4() }}
            </div>
        </div>
        <div :class="this.level5 > 70 ? 'level': 'level shakey'" id="pyramid-level-5">
            <div class="inside-text">
            {{ calcTotalLevel5() }}
            </div>
        </div>
    </div>
    <div class="diagnosis">
      here is the results cases
      <div>
        <h1 class="blue" >Self Actualization</h1>
        Self-actualization is a lifelong journey, and certainly not a
        state to achieve once, but something to strive for by making
        sure the different areas of your life are as balanced as possible,
        making you more likely to experience personal growth and self-awareness,
        creativity, lack of prejudice and radical acceptance of facts
      </div>
      <div class="esteem">
        <h1 class="green" >Esteem</h1>
        <div v-if='this.average2 < 70' class="esteem-0">
        The need for a solid positive sense of self and the desire to get along
        well with others is human nature. Feeling unsteady at this level can
        lead to feelings of low self-worth, low confidence, low self-esteem,
        imposter syndrome and social anxiety. Addressing acceptance of yourself
        and others is a core concept in cognitive behavioral therapy.
        </div>
        <div v-if='this.average2 >= 70' class="esteem-70">
        Everyone gets down on themselves sometimes, but it seems like you feel
        like you’re doing okay more often than not.  Assertiveness and a solid
        sense of self will do much better in the long run than an inflated sense
        of self-esteem and a narcissistic streak. Feeling mostly steady at this
        level will help you go back and firm up any shaky needs in other areas.
        </div>
      </div>
      <div class="love">
        <h1 class="red" >Love and Belonging</h1>
        <div v-if='this.average3 < 70' class="love-0">
          Humans are social creatures. Feeling disconnected, isolated, alienated,
          misunderstood and alone leads to depression, despair, resentment and
          social anxiety, and ultimately existential dread. Stabilizing this
          level might mean working on communication, improving and increasing
          sexual intimacy as well as emotional intelligence (and intimacy).
          Therapy can address this area by helping you to better understand
          your relationship to others while you’re on the planet.
        </div>
        <div v-if='this.average3 >= 70' class="love-70">
          Regardless of who you call your friends and family, you know that you
          belong and are loved. Counseling can make sure you master interpersonal
          relationships and help you address minor conflicts in sex, love and social
          life before they become emotional cutoffs and crises.
        </div>
      </div>
      <div class="safety">
        <h1 class="purple" >Safety</h1>
        <div v-if='this.average4 < 70 ' class="safety-0">
          Feeling unsafe in your day to day existence, even at a low level, can cause
          so much stress that you will feel it in almost every other area of your life.
          This might mean minority stress and dealing with micro-aggressions every day,
          or it might mean your apartment feels more like a prison than a sanctuary.
          Counseling might not be able to address all of your safety concerns, but your
          therapist can refer you to all types of resources to help you address your
          safety needs.
        </div>
        <div v-if='this.average4 >= 70' class="safety-70">
          The world is a dangerous place, but you’re lucky to count yourself as
          someone who feels generally safe in it. Good on you! Feeling solid at
          this level gives you a fairly solid foundation to build on career,
          relationships and other passions.
        </div>
      </div>
      <div class="psychological">
        <h1 class="yellow" >Physiological</h1>
        <div v-if='this.average5 < 70' class="psycho-0">
          This is the foundational needs level for all humans, according to Maslow’s
          Theory of Motivation. Having a fragile relationship to food, or sex or air
          or water might mean not having healthy access to it (healthy food and
          pollution-free air and water), or it might mean having an unhealthy
          relationship with it. Sleep is also at this level. Too much sleep can
          be a sign of depression.  Too little can mean insomnia and a diminished
          ability to deal with stress. Of course we can’t skip sex! You might not
          die if you don’t have sex, but are you really living if you have sexual
          baggage to deal with? A healthy sexual outlet is as necessary for the
          human animal as access to food, water, warmth and sleep.
        </div>
        <div v-if='this.average5 >= 70' class="psycho-70">
          You have a basic handle on your basic needs, and maintaining that balance
          of healthy nutrition, hydration, and sexual expression will help propel
          you towards self-actualization. You’ve got a solid foundation.  Checking
          in with counseling can help you recognize problem areas before they become
          crises.
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
