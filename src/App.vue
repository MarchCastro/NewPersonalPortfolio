<template>
  <div id="app">
    <ul id="nav">
      <li>
        <a href="#homeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/Menu_option.svg')"></div>
          <div class="option"> Menu </div>
        </a>
      </li>

      <li>
        <a href="#homeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/Home_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu-img/Home_option_hover.svg')"></div>
          <div class="option"> Home </div>
        </a>
      </li>
  
      <li>
        <a href="#aboutMeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/About_menu_option.svg')"></div>
          <div class="option"> About me </div>
        </a>
      </li>

      <li>
        <a href="#experienceCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/Experience_option.svg')"></div>
          <div class="option"> Experience </div>
        </a>
      </li>

      <li>
        <a href="#portfolioCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/Portfolio_option.svg')"></div>
          <div class="option"> Portfolio </div>
        </a>
      </li>

      <li>
        <a href="#educationCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu-img/Education_option.svg')"></div>
          <div class="option"> Education </div>
        </a>
      </li>
    </ul>

    <HomeCard/>
    <AboutMeCard/>
    <ProfessionalBackgroundCard/>
    <ExperienceCard/>
    <PortfolioCard/>
    <EducationCard/>

    <portfolioModal :active="modal.active && modal.current === 'portfolio'"/>
    <!-- other modals -->

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
    background: #b75e5f
    border-top-right-radius: 14px
    border-bottom-right-radius: 14px
    height: 365px
    left: 1
    margin-top: 180px
    padding: 48px 0 0 0
    position: fixed
    text-align: center
    width: 100px
    z-index: 2

    .option-icon
      background-position: center
      background-repeat: no-repeat
      background-size: contain
      cursor: pointer
      height: 22px
      left: -50px
      position: absolute
      top: -7px
      width: 100px

    .option 
      color: #fff
      font-family: 'CarosLight'
      font-size: 10px
      text-decoration: none
    
    a
      position: relative
      text-decoration: none
    
    li 
      list-style-type: none
      margin-bottom: 47px
    
    .option:hover
      color: #352d39

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
