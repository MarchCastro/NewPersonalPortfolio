<template>
  <div id="portfolioCard" class="section">
    <div class="card">
      <!-- Decoration ovals -->
      <div class="oval one purple-one"></div>
      <div class="oval two purple-four"></div>
      <div class="oval three purple-three"></div>
      <!--<div class="oval four purple-two"></div>
      <div class="oval five purple-one"></div>
      <div class="oval six purple-two"></div>-->

      <!-- Title page -->
      <div class="title-page"> Portfolio </div>
      <div class="subtitle-page"> Have a look to all my work </div>
      <!-- <div class="subtitle-section"> Display mockups </div> -->
      <!-- Cards-->
      <div class="cards"> 

        <!-- Actual portfolio -->
        <div class="portfolio-item green-card">
          <img class="image" src="../assets/img/Actual_portfolio.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>

        <!-- Past portfolio -->
        <div class="portfolio-item blue-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Last_portfolio.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Past Portfolio </a>
          </div>
        </div>

        <!-- Library practice -->
        <div class="portfolio-item purple-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Library_practice.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
      </div>

      <!-- <div class="subtitle-section"> App mockups </div> -->
      <div class="cards"> 
        
        <!-- Sapphire app -->
        <div class="portfolio-item green-card" v-on:click="openModal('portfolio')">
          <img class="mobile-image" src="../assets/img/Sapphire_1.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- Demente app -->
        <div class="portfolio-item blue-card" v-on:click="openModal('portfolio')">
          <img class="mobile-image" src="../assets/img/Demente_1.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- Heartbeat app -->
        <div class="portfolio-item purple-card" v-on:click="openModal('portfolio')">
          <img class="mobile-image" src="../assets/img/Heartbeat_1.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
      </div>
      

      <!-- <div class="subtitle-section"> Wireframes and sketches </div> -->
      <div class="cards"> 
        
        <!-- Wireframe Virgin Galactic -->
        <div class="portfolio-item green-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Wireframe_VG.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- UserFlow Virgin Galactic -->
        <div class="portfolio-item blue-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/UserFlow_VG.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- TaskFlow Virgin Galactic -->
        <div class="portfolio-item purple-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/TaskFlow_VG.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
      </div>

      <div class="cards">  
        <!-- Dog App Sitemap -->
        <div class="portfolio-item green-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Sitemap_1.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- Dog Door Interaction Map -->
        <div class="portfolio-item purple-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/DoggieDoor_InteractionMap.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>

        <!-- Shoe Store Content map -->
        <div class="portfolio-item blue-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/ShoeStore_ContentMap.png">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
      </div>

      <div class="cards">  
        <!-- Dog App Sketch -->
        <div class="portfolio-item green-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Sketch_3.jpeg">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
        
        <!-- Virgin Galactic Sketc -->
        <div class="portfolio-item purple-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Sketch_1.jpeg">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>

        <!-- Shoe Store Content map -->
        <div class="portfolio-item blue-card" v-on:click="openModal('portfolio')">
          <img class="image" src="../assets/img/Sketch_2.jpeg">
          <div class="overlay">
            <a href="www.facebook.com" target="_blank" class="text-overlay"> Actual Portfolio </a>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
import router from '../router'

export default {
  methods: {
    openModal (modal) {
      router.push({ path: '', query: { modal: modal } })
      // this.$route = {modal: true, current: modal}
    }
  },
  name: 'portfolioCard'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import "@/variables.sass"

  .title-page
    color: #364252
    font-family: 'CarosMedium'
    font-size: 40px
    margin-left: 67px
    margin-top: 90px
  
  .subtitle-page
    color: #364252
    font-family: 'CarosMedium'
    font-size: 18px
    margin-bottom: 38px
    margin-left: 67px
  
  .subtitle-section
    color: #364252
    font-family: 'CarosLight'
    font-size: 21px
    margin-left: 67px
    margin-top: 38px

  .cards
    margin: 15px 80px 0 80px
    width: calc(100% - 160px)

    .portfolio-item
      border-radius: 8px
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
      display: inline-block
      height: 261px
      margin-bottom: 30px
      margin-right: 60px
      width: calc(100%/3 - 40px)
    
      &:last-child
        margin-right: 0
      
      &.green-card
      background: $soft-green

      &.blue-card
        background: $soft-blue

      &.purple-card
        background: $soft-purple
      
      .image
          display: block
          height: 207px
          margin: 20px 20px
          min-width: calc(100% - 40px)
      
      .mobile-image
          display: block
          height: 207px
          margin: 20px 90px
          min-width: calc(100% - 180px)
  
      .overlay 
        background-color: #414141
        bottom: 0
        height: 0
        left: 0
        opacity: 0.86
        overflow: hidden
        position: absolute
        right: 0
        transition: .5s ease
        width: 100%

        .text-overlay 
          color: #fff
          font-family: 'CarosLight'
          font-size: 14px
          margin: 18px
          text-decoration: none
          position: absolute
      
        &:hover .overlay 
          height: 100%
  
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

  @media screen and (min-width: 1440px)
    .oval
      &.one
        height: 79px
        left: 1176px
        top: 26px
        width: 79px

      &.two
        height: 15px
        left: 1290px
        top: 36px
        width: 15px

      &.three
        height: 51px
        left: 1247px
        top: 83px
        width: 51px

      &.four
        height: 38px
        left: 57px
        top: 822px
        width: 38px

      &.five
        height: 31px
        left: 98px
        top: 844px
        width: 31px

      &.six
        height: 15px
        left: 64px
        top: 868px
        width: 15px

</style>
