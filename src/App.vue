<template>
  <div id="app">
    <ul id="nav" v-scroll-spy-active v-scroll-spy-link>
      <li>
        <a href="#homeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Menu_option.svg')"></div>
          <div class="option_header"> Menu </div>
        </a>
      </li>

      <li>
        <a href="#homeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Home_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu/Home_option_hover.svg')"></div>
          <div class="option"> Home </div>
        </a>
      </li>
  
      <li>
        <a href="#aboutMeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/About_menu_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu/About_menu_option_hover.svg')"></div>
          <div class="option"> About me </div>
        </a>
      </li>

      <li>
        <a href="#experienceCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Experience_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu/Experience_option_hover.svg')"></div>
          <div class="option"> Experience </div>
        </a>
      </li>

      <li>
        <a href="#portfolioCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Portfolio_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu/Portfolio_option_hover.svg')"></div>
          <div class="option"> Portfolio </div>
        </a>
      </li>

      <li>
        <a href="#educationCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Education_option.svg')"></div>
          <div class="option-icon hover" style="backgroundImage:url('/img/menu/Education_option_hover.svg')"></div>
          <div class="option"> Education </div>
        </a>
      </li>
    </ul>
    
    <div v-scroll-spy>
      <div></div>
      <HomeCard/>
      <AboutMeCard/>
      <!-- <ProfessionalBackgroundCard/> -->
      <ExperienceCard/>
      <PortfolioCard/>
      <EducationCard/>
    </div>

    <portfolioModal :active="modal.active && modal.current === 'portfolio'"/>
    <certificateModal :active="modal.active && modal.current === 'certificate'" />
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
import certificateModal from './components/certificateModal.vue'

import router from './router'

import Vue from 'vue'
import Scrollspy from 'vue2-scrollspy'
// use default options
Vue.use(Scrollspy)

// or custom options
Vue.use(Scrollspy, {})

export default {
  name: 'app',
  components: {
    HomeCard,
    AboutMeCard,
    //ProfessionalBackgroundCard,
    PortfolioCard,
    ExperienceCard,
    EducationCard,
    certificateModal,
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
      router.push({ query: {} })
    },
    openModal (modal) {
      router.push({ path: '', query: { modal: modal } })
      // this.$route = {modal: true, current: modal}
    }
  },
  mounted () {
    document.onkeydown = function(evt) {
      evt = evt || window.event
      // eslint-disable-next-line
      console.log(evt.keyCode)
      
      if (evt.keyCode == 27) {
        router.push({ query: {} })
      }
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

    .option_header 
      color: #fff
      font-family: 'CarosLight'
      font-size: 10px
      text-decoration: none
    
    .option 
      color: #fff
      font-family: 'CarosLight'
      font-size: 10px
      text-decoration: none
    
    a
      position: relative
      text-decoration: none

      .option-icon.hover
        opacity: 0
    
    li 
      list-style-type: none
      margin-bottom: 47px

      &.active
        color: #352d39

        .option
          color: #352d39

        .option-icon.hover
          opacity: 1
    
    a:hover
      .option
        color: #352d39

      .option-icon.hover
        opacity: 1

  #app
    background-color: #321f37
    min-height: calc(100vh - 120px)
    font-family: 'CarosLight'

  .nav
    background: purple
    left: 0
    min-height: 200px
    position: fixed
    top: 0
    width: 120px
    z-index: 2

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
