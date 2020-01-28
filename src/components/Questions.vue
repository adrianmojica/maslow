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
      value_5: 0
    }
  }
}
</script>

<template>
  <div>
    <p>this is the copy explaining what to do</p>
    <div class="container">
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
    </div>
    <Pyramid/>
    Self Actualization {{ value_1 }}
    Esteem {{ value_2 }}
    Love {{ value_3 }}
    Safety {{ value_4 }}
    Physiological {{ value_5 }}

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
</style>
