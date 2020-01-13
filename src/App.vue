<template>
  <div id="app">
    <HomeCard/>
  </div>
</template>

<script>
import HomeCard from './components/HomeCard.vue'

export default {
  name: 'app',
  components: {
    HomeCard
  }
}
</script>

<style lang="sass">
  html, body
    margin: 0
    padding: 0

  #app
    background-color: #321f37
    min-height: 100vh

  .card
</style>
