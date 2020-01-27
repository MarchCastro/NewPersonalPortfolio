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
        <a href="#professionalBackgroundCard"> about 2</a>
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
    <ProfessionalBackgroundCard/>
    <PortfolioCard/>
    <ExperienceCard/>
    <EducationCard/>

    <portfolioModal :active="modal.active && modal.current === 'portfolio'"/>
    // other modals

    <div id="modalOverlay"
         v-bind:class="{active: query.modal !== undefined}"
         v-on:click="closeModal()"></div>

  </div>
</template>

<script>
import HomeCard from './components/HomeCard.vue'
import AboutMeCard from './components/AboutMeCard.vue'
//import ProfessionalBackgroundCard from './components/ProfessionalBackgroundCard.vue'
import PortfolioCard from './components/PortfolioCard.vue'
import ExperienceCard from './components/ExperienceCard.vue'
import EducationCard from './components/EducationCard.vue'

import portfolioModal from './components/portfolioModal.vue'

import router from './router'

export default {
  name: 'app',
  components: {
    HomeCard,
    AboutMeCard,
    //ProfessionalBackgroundCard,
    PortfolioCard,
    ExperienceCard,
    EducationCard,
    portfolioModal
  },
  computed: {
    query () {
      return this.$route.query
    }
  },
  data: function () {
    return {
      modal: {
        active: true,
        current: 'portfolio'
      }
    }
  },
  methods: {
    closeModal () {
      router.push({ path: '', query: {} })
    },
    openModal (modal) {
      router.push({ path: '', query: { modal: modal } })
      // this.$route = {modal: true, current: modal}
    }
  }
}
</script>

<style lang="sass">
  html, body
    margin: 0
    padding: 0

  @font-face
    font-family: 'CarosLight'
    src: url('assets/fonts/CarosLight.otf')

  @font-face
    font-family: 'CarosBold'
    src: url('assets/fonts/CarosBold.otf')

  @font-face
    font-family: 'CarosMedium'
    src: url('assets/fonts/CarosMedium.otf')

  #nav
    background: orange
    position: fixed
    right: 0

  #app
    background-color: #321f37
    min-height: calc(100vh - 120px)
    font-family: 'CarosLight'

  .section    
    height: 100vh
    padding-left: 50px
    padding-top: 30px
    width: calc(100vw - 100px)

    &:last-child
      height: calc(100vh - 30px)

    .card
      background: #FFF
      border-radius: 32px
      height: calc(100vh - 60px)
      max-width: 1340px
      overflow: hidden
      position: relative
      width: calc(100vw - 100px)

  #modalOverlay
    background: #000
    height: 100vh
    left: 0
    opacity: 0
    pointer-events: none
    position: fixed
    top: 0
    transition: all 0.3s
    width: 100vw
    z-index: 9

    &.active
      opacity: 0.9
      pointer-events: all

  @media screen and (min-width: 1440px)
    .card
      margin: 0 auto

</style>
