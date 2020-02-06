<script>

import VueSlider from 'vue-slider-component'
import Pyramid from '../components/Pyramid.vue'
import 'vue-slider-component/theme/material.css'

export default {
  name: 'Questions',
  components: {
    VueSlider,
    Pyramid
  },
  data: function () {
    return {
      value_1: 0,
      value_2: 0,
      value_2_1: 0,
      value_2_2: 0,
      value_2_3: 0,
      value_2_4: 0,
      value_2_5: 0,
      value_3: 0,
      value_3_1: 0,
      value_3_2: 0,
      value_3_3: 0,
      value_4: 0,
      value_4_1: 0,
      value_4_2: 0,
      value_4_3: 0,
      value_4_4: 0,
      value_5: 0,
      value_5_1: 0,
      value_5_2: 0,
      value_5_3: 0,
      value_5_4: 0,
      value_5_5: 0,
      value_5_6: 0,
      isHidden: false
    }
  },
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
  }
}
</script>

<template>
  <div class="copy">
    <h1>Maslow's Hierarchy of Needs</h1>
    <p>
      Maslow's hierarchy of needs is a theory in psychology
      that is formed of a five-tier model of human needs,
      depicted as the levels of a pyramid.
      Needs lower down in the pyramid must be satisfied before
      individuals can attend to any of the needs in the higher up steps.
    </p>
    <p>
      In the next exercise we ask you to move the slider to the sides according to
      how well met the need is in your life. 0, the lowest value, means that currently
      the need is not being met, while 100 means the need is met and healthy.
    </p>

    <div v-if="!isHidden" class="container">
      <div class="controls">
        <!-- Self Actualization -->
        <div class="label">Desire to be the most that one can be</div>
        <VueSlider v-model="value_1" :lazy="true"></VueSlider>
        <!-- Esteem -->
        <div class="label">Respect</div>
        <VueSlider v-model="value_2"></VueSlider>
        <div class="label">Self Esteem</div>
        <VueSlider v-model="value_2_1"></VueSlider>
        <div class="label">Status</div>
        <VueSlider v-model="value_2_2"></VueSlider>
        <div class="label">Recognition</div>
        <VueSlider v-model="value_2_3"></VueSlider>
        <div class="label">Strength</div>
        <VueSlider v-model="value_2_4"></VueSlider>
        <div class="label">Freedom</div>
        <VueSlider v-model="value_2_5"></VueSlider>
        <!-- Love and Belonging -->
        <div class="label">Friendship</div>
        <VueSlider v-model="value_3"></VueSlider>
        <div class="label">Intimacy</div>
        <VueSlider v-model="value_3_1"></VueSlider>
        <div class="label">Family</div>
        <VueSlider v-model="value_3_2"></VueSlider>
        <div class="label">Sense of Connection</div>
        <VueSlider v-model="value_3_3"></VueSlider>
        <!-- safety -->
        <div class="label">Personal Security</div>
        <VueSlider v-model="value_4"></VueSlider>
        <div class="label">Employment</div>
        <VueSlider v-model="value_4_1"></VueSlider>
        <div class="label">Resources</div>
        <VueSlider v-model="value_4_2"></VueSlider>
        <div class="label">Health</div>
        <VueSlider v-model="value_4_3"></VueSlider>
        <div class="label">Property</div>
        <VueSlider v-model="value_4_4"></VueSlider>
        <!-- Physiological -->
        <div class="label">Air</div>
        <VueSlider v-model="value_5"></VueSlider>
        <div class="label">Water</div>
        <VueSlider v-model="value_5_1"></VueSlider>
        <div class="label">Food</div>
        <VueSlider v-model="value_5_2"></VueSlider>
        <div class="label">Shelter</div>
        <VueSlider v-model="value_5_3"></VueSlider>
        <div class="label">Sleep</div>
        <VueSlider v-model="value_5_4"></VueSlider>
        <div class="label">Clothing</div>
        <VueSlider v-model="value_5_5"></VueSlider>
        <div class="label">Sex</div>
        <VueSlider v-model="value_5_6"></VueSlider>
        <button class="result" v-on:click="isHidden = true"> results</button>
      </div>
      <div class="explain">
        What we will do now is average your needs and check what are the parts that
        are lacking some care in your life. If there is anything shakey, the pyramid will be unstable,
        and therefore life could feel like its hard. if sectors of your life are shakey in the lower levels
        it can feel like needs in higher levels are harder to meet as well.
      </div>
    </div>
    <Pyramid v-if="isHidden" :level1= value_1 :level2=value_2 :level2_1=value_2_1 :level2_2=value_2_2 :level2_3=value_2_3 :level2_4=value_2_4 :level2_5=value_2_5
    :level3=value_3 :level3_1=value_3_1 :level3_2=value_3_2 :level3_3=value_3_3 :level4=value_4 :level4_1=value_4_1 :level4_2=value_4_2 :level4_3=value_4_3
    :level4_4=value_4_4 :level5=value_5 :level5_1=value_5_1 :level5_2=value_5_2 :level5_3=value_5_3 :level5_4=value_5_4
    :level5_5=value_5_5 :level5_6=value_5_6 />
    <div v-if="isHidden" class="diagnosis">
      here is the results cases
      <div><h1 class="blue" >Self Actualization</h1></div>
      <div><h1 class="green" >Esteem</h1></div>
      <div><h1 class="red" >Love and Belonging</h1></div>
      <div><h1 class="purple" >Safety</h1></div>
      <div><h1 class="yellow" >Physiological</h1></div>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
  width:auto;
  margin:auto;
  margin-bottom: 50px;
  .controls{
    max-width: 450px;
    text-align: center;
    margin: auto;
  }
  .result {
    text-align: center;
    margin-top: 30px;
    width: 240px;
    margin-left: 90px;
    height: 45px;
  }
  .explain {
    margin-top:20px;
  }
}
h1 {
  text-align: center;
}
.copy {
  margin: 0 auto;
  padding-left: 20%;
  padding-right: 20%;
  text-align: justify;
}

button {
  display:inline-block;
  background: #0053ee;
  height:25px;
  font-size: 18px;
  width:100px;
  padding:0.3em 1.2em;
  margin:0 0.1em 0.1em 0;
  border:0.16em solid rgba(255,255,255,0);
  border-radius:2em;
  box-sizing: border-box;
  text-decoration:none;
  font-family:'Roboto',sans-serif;
  font-weight:300;
  color:#FFFFFF;
  text-shadow: 0 0.04em 0.04em rgba(0,0,0,0.35);
  text-align:center;
  transition: all 0.2s;
}
button :hover{
  border-color: rgba(255,255,255,1);
}

.diagnosis {
  .blue {
    text-align:left;
    color:#0053ee;
  }
  .green {
    text-align:left;
    color:green;
  }
  .red {
    text-align:left;
    color:red;
  }
  .purple {
    text-align:left;
    color: purple;
  }
  .yellow {
    text-align:left;
    color: orange;
  }
}

@media all and (max-width:30em){
  button {
    display:block;
    margin:0.2em auto;
  }
}
</style>
