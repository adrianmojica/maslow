<script>

import VueSlider from 'vue-slider-component'
import Pyramid from '../components/Pyramid.vue'
import 'vue-slider-component/theme/default.css'

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
      value_3: 0,
      value_4: 0,
      value_5: 0,
      isHidden: false
    }
  },
  props: {
    level1: Number,
    level2: Number,
    level3: Number,
    level4: Number,
    level5: Number
  }
}
</script>

<template>
  <div>
    <p>this is the copy explaining what to do</p>
    <div v-if="!isHidden" class="container">
      <div class="controls">
      <div class="label">Self Actualization</div>
      <VueSlider v-model="value_1" :lazy="true"></VueSlider>
      <div class="label">Esteem</div>
      <VueSlider v-model="value_2"></VueSlider>
      <div class="label">Love/Belonging</div>
      <VueSlider v-model="value_3"></VueSlider>
      <div class="label">Safety</div>
      <VueSlider v-model="value_4"></VueSlider>
      <div class="label">Physiological</div>
      <VueSlider v-model="value_5"></VueSlider>
      </div>
      <button v-on:click="isHidden = true"> results</button>
    </div>
    <Pyramid v-if="isHidden" :level1= value_1 :level2=value_2 :level3=value_3 :level4=value_4 :level5=value_5 />
    <!-- Self Actualization {{ value_1 }}
    Esteem {{ value_2 }}
    Love {{ value_3 }}
    Safety {{ value_4 }}
    Physiological {{ value_5 }} -->

    <!-- send values to pyramid with button and questions dissappear -->

  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
  width:400px;
  margin:auto;
  .controls{
    max-width: 450px;
  }
}
button {
  display:inline-block;
  background: #E91E63;
  height:25px;
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
@media all and (max-width:30em){
  button {
    display:block;
    margin:0.2em auto;
  }
}
</style>
