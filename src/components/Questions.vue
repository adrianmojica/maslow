<script>

import VueSlider from 'vue-slider-component'
import 'vue-slider-component/theme/default.css'

export default {
  name: 'Questions',
  components: {
    VueSlider
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
    <p>HI</p>
    Self Actualization
    <VueSlider v-model="value_1" :lazy="true"></VueSlider>
    Esteem
    <VueSlider v-model="value_2"></VueSlider>
    Love/Belonging
    <VueSlider v-model="value_3"></VueSlider>
    Safety
    <VueSlider v-model="value_4"></VueSlider>
    Physiological
    <VueSlider v-model="value_5"></VueSlider>

    Self Actualization {{ value_1 }}
    Esteem {{ value_2 }}
    Love {{ value_3 }}
    Safety {{ value_4 }}
    Physiological {{ value_5 }}

  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
