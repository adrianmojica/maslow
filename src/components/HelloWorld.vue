<template>
  <div class="hello">
    <Questions/>
  </div>
</template>

<script>
import Questions from './components/Questions.vue'

export default {
  name: 'HelloWorld',
  components: {
    Questions: Questions
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
