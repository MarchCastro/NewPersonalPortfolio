<template>
  <div id="app">
    <HomeCard/>
    <AboutMeCard/>
    <PortfolioCard/>
    <ExperienceCard/>
    <EducationCard/>
  </div>
</template>

<script>
import HomeCard from './components/HomeCard.vue'
import AboutMeCard from './components/AboutMeCard.vue'
import PortfolioCard from './components/PortfolioCard.vue'
import ExperienceCard from './components/ExperienceCard.vue'
import EducationCard from './components/EducationCard.vue'

export default {
  name: 'app',
  components: {
    HomeCard,
    AboutMeCard,
    PortfolioCard,
    ExperienceCard,
    EducationCard
  }
}
</script>

<style lang="sass">
  html, body
    margin: 0
    padding: 0

  #app
    background-color: #321f37
    min-height: calc(100vh - 50px)
    padding-top: 50px

  .card
    background: #FFF
    border-radius: 14px
    height: calc(100vh - 100px)
    margin: 0 0 50px 50px
    width: calc(100vw - 100px)


</style>
