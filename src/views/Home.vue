<template>
  <div class="home">
    <Questions/>
     <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Questions from '@/components/Questions.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'home',
  components: {
    Questions,
    Footer
  }
}
</script>

<style scoped>
  .home {
      margin-top: 50px;
  }
</style>
