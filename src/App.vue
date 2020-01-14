<template>
  <div id="app">
    <ul id="nav">
      <li>
        <a href="#homeCard"> home </a>
      </li>
  
      <li>
        <a href="#aboutMeCard"> about </a>
      </li>

      <li>
        <a href="#portfolioCard"> portfolio </a>
      </li>

      <li>
        <a href="#experienceCard"> experience </a>
      </li>

      <li>
        <a href="#educationCard"> education </a>
      </li>
    </ul>

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

  #nav
    background: orange
    position: fixed
    right: 0

  #app
    background-color: #321f37
    min-height: calc(100vh - 100px)

  .section    
    height: 100vh
    padding-left: 50px
    padding-top: 50px
    width: calc(100vw - 100px)

    &:last-child
      height: calc(100vh - 50px)

    .card
      background: #FFF
      border-radius: 14px
      height: calc(100vh - 100px)
      width: calc(100vw - 100px)


</style>
