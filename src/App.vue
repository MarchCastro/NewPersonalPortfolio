<template>
  <div id="app">
    <ul id="nav" v-scroll-spy-active v-scroll-spy-link>
      <!--<li>
        <a href="#homeCard">
          <div class="option-icon" style="backgroundImage:url('/img/menu/Menu_option.svg')"></div>
          <div class="option_header"> Menu </div>
        </a>
      </li>-->

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

    <!-- <div id="no-compatible-resolution" v-bind:class="{active: query.modal === 'no-compatible'}"></div> -->
    <div class="construction" v-bind:class="{active: query.modal === 'no-compatible'}"> 
      <div class="content">
        <div class="title">We're still under construction</div>
        <div class="image" style="backgroundImage: url('/videos/responsive_modal.gif')"></div>
        <div class="description">Sorry for the interaction problems, this website is still getting ready.
          For a better visualization, the best resolution screen is 1440px. <br><br>
        Thanks for understanding.
        </div>
      </div>
    </div>
    
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
    
    const vw = Math.max(document.documentElement.clientWidth, window.innerWidth || 0);
    
    if (vw < 1438) {
      router.push({ path: '', query: { modal: 'no-compatible' } })
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
    height: 378px
    left: 0
    margin-top: 180px
    padding: 10px 0 0 0
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
      left: 0
      position: absolute
      top: 19px
      width: 100px

    .option_header 
      color: #fff
      font-family: 'CarosLight'
      font-size: 10px
      text-decoration: none
    
    .option
      bottom: 0
      color: #fff
      font-family: 'CarosLight'
      font-size: 10px
      position: absolute
      text-align: center
      text-decoration: none
      width: 100%
    
    a
      display: block
      height: 56px
      position: relative
      text-decoration: none
      width: 100px

      .option-icon.hover
        opacity: 0
    
    li
      height: 56px
      list-style-type: none
      margin-bottom: 16px

      &.active
        color: #352d39

        .option
          color: #352d39

        .option-icon
          opacity: 0

        .option-icon.hover
          opacity: 1
    
    a:hover
      .option
        color: #352d39

      .option-icon
        opacity: 0

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

  #no-compatible-resolution
    background: #000
    color: red
    height: 100vh
    left: 0
    opacity: 0
    pointer-events: none
    position: fixed
    top: 0
    transition: all 0.3s
    width: 100vw
    z-index: 200

    &.active
      opacity: 0.8
      pointer-events: all

  .construction
    background: #FFF
    border-radius: 4px
    height: 500px
    margin: auto 350px 
    opacity: 0
    pointer-events: none
    position: fixed
    top: 150px
    transition: all 0.3s
    vertical-align: center
    width: calc(100% - 700px)
    z-index: 10

    &.active
      opacity: 1
      pointer-events: all
    
    .content
      margin: 50px 40px 50px 40px
      width: calc(100% - 80px)
      
      .title
        color: #573350
        display: block
        font-family: 'CarosBold'
        font-size: 25px
        text-align: center
        text-transform: uppercase

        .subtitle
          text-align: center
      
      .description
        color: #573350
        font-family: 'CarosLight'
        font-size: 15px
        text-align: justify
      
      .image
          background: no-repeat
          background-size: contain
          background-position: center
          height: 280px
          opacity: 1
          width: calc(100%)

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

  @media screen and (min-width: 1400px)
    #no-compatible-resolution
      display: none
    .construction
      display: none

    .card
      margin: 0 auto

</style>
