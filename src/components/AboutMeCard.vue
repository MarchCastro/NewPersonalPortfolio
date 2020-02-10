<template>
  <div id="aboutMeCard" class="section">
    <div class="card">
      <div class="first slider-section" v-bind:class="{hidden: section === 1}">
        <!-- Picture ovals -->
        <div class="oval one purple-one"></div>
        <div class="oval two purple-two"></div>
        <div class="oval three purple-one"></div>
        <div class="oval four purple-three"></div>
        <div class="oval five purple-two"></div>
        <div class="oval six purple-four"></div>
        <div class="oval seven purple-four"></div>
        <div class="oval eight purple-one"></div>
        <div class="oval nine purple-two"></div>

        <img class="profile-picture" src="../assets/img/about-me@3x.png">

        <div class="title-page"> Who am I? </div>

        <div class="description"> I’m a Software Engineer with a growing interest on UI/UX Design from Mexico City. I recently discovered that in this area I can explote all my passions such as designing and drawing.
          <br> <br>I know that no mather how much time I spend working, I won't get bored because at the end it's all about making art and doing what you love. </div>

        <!-- Passions icons -->
        <div class="passion-icon-div">
          <img class="passion-icon" src="../assets/img/flat-icon-sax.png">
          <img class="passion-icon" src="../assets/img/flat-icon-cinema.png">
          <img class="passion-icon" src="../assets/img/flat-icon-dog2.png">
          <img class="passion-icon" src="../assets/img/flat-icon-travel.png">
          <img class="passion-icon" src="../assets/img/flat-icon-draw.png">
        </div>
        <a href="/MarcelaCastroFlores_CV_vE_v2-2.pdf" download>
          <button class="button-cv">Download CV</button>
        </a>
      </div>

      <div class="second slider-section" v-bind:class="{hidden: section === 1}">
        <professionalKnowledge />
      </div>
      
      <!-- Slider options -->
      <div class="slider-options">
        <div class="option one"
             v-on:click="section = 0"
             v-bind:class="{active: section === 0}">
          <div class="number"> 1 </div>
          <div class="actual-slider-text"> Who am I? </div>
        </div>
        
        <hr>
        
        <div class="option two"
             v-on:click="section = 1"
             v-bind:class="{active: section === 1}">
          <div class="number"> 2 </div>
          <div class="actual-slider-text"> Professional background </div>
        </div>
      </div>
         
    </div>
  </div>
</template>

<script>
import professionalKnowledge from './ProfessionalKnowledgeCard'

export default {
  components: {
    professionalKnowledge: professionalKnowledge
  },
  data: function () {
    return {
      section: 0
    }
  },
  name: 'AboutMeCard'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import "@/variables.sass"

  .card
    max-height: calc(100vh - 60px)
    white-space: nowrap

  .slider-section
    display: inline-block
    height: calc(100vh - 60px)
    transition: all 0.3s
    transform: translate3d(0, 0, 0)
    vertical-align: top
    width: 100%
    
    &.hidden
      transform: translate3d( calc(-100vw + 50px), 0, 0)

  .oval
    border-radius: 50%
    position: absolute

    &.purple-one
      background: $purple-one

    &.purple-two
      background: $purple-two

    &.purple-three
      background: $purple-three

    &.purple-four
      background: $purple-four

  .profile-picture
    height: 192px
    left: 225px
    position: absolute
    top: 184px
    width: 192px
  
  .title-page
    color: #364252
    font-family: 'CarosMedium'
    font-size: 40px
    margin-left: 597px
    margin-top: 143px
  
  .description
    color: #364252
    font-family: 'CarosLight'
    font-size: 14px
    margin-left: 597px
    margin-top: 20px
    margin-right: 164px
    text-align: justify
    white-space: normal
  
  .button-cv
    background-color: #b75e5f
    border: none
    border-radius: 4px
    color: white
    cursor: pointer
    font-family: 'CarosMedium'
    font-size: 14px
    height: 36px
    margin-left: 1012px
    margin-top: 46px
    outline: none
    width: 165px
  
  .button-cv:hover
    background-color: #fff
    border: 2px solid #b75e5f
    color: #b75e5f

  .passion-icon-div 
    margin-left: 597px
    margin-top: 29px

  .passion-icon
    height: 41px    
    margin-right: 16px
    width: 41px

  .slider-options
    bottom: 96px
    height: 64px
    position: absolute
    right: 164px
    vertical-align: top
    width: 360px

    .option
      cursor: pointer
      display: inline-block
      font-size: 15px

      &:first-child
        margin-right: 82px

      .number
        background: #805B6F
        border-radius: 50%
        color: #FFF
        height: 29px
        line-height: 29px
        margin: 0 auto
        margin-bottom: 8px
        text-align: center
        transform: scale3d( 1, 1, 1)
        transition: all 0.3s
        width: 29px

      &.active
        .number
          background: #52354F
          transform: scale3d(1.3, 1.3, 1)

    hr
      border-bottom: none
      border-top: dotted 5px
      left: 55px
      margin: 0
      height: 1px
      position: absolute
      top: 12px
      width: 180px
        
  @media screen and (min-width: 1440px)
    .oval
      &.one
        height: 35px
        left: 192px
        top: 159px
        width: 35px

      &.two
        height: 9px
        left: 302px
        top: 148px
        width: 9px

      &.three
        height: 129px
        left: 369px
        top: 143px
        width: 129px

      &.four
        height: 84px
        left: 169px
        top: 270px
        width: 84px

      &.five
        height: 28px
        left: 474px
        top: 313px
        width: 28px

      &.six
        height: 58px
        left: 243px
        top: 390px
        width: 58px

      &.seven
        height: 111px
        left: 350px
        top: 309px
        width: 111px

      &.eight
        height: 23px
        left: 350px
        top: 436px
        width: 23px

      &.nine
        height: 9px
        left: 465px
        top: 449px
        width: 9px

</style>
