<template>
  <div id="portfolioCard" class="section">
    <div class="card">
      <!-- Decoration ovals -->
      <div class="oval one purple-one"></div>
      <div class="oval two purple-four"></div>
      <div class="oval three purple-three"></div>
      <div class="oval four purple-two"></div>
      <div class="oval five purple-one"></div>
      <div class="oval six purple-two"></div>

      <!-- Title page -->
      <div class="title-page"> Portfolio </div>
      <div class="subtitle-page"> Have a look to all my work </div>

      <!-- Cards-->
      <div class="cards"> 
        <div class="portfolio-item" v-on:click="openModal('portfolio')">
          Hola
        </div>
        <div class="portfolio-item" v-on:click="openModal('portfolio')">
          Hola
        </div>
        <div class="portfolio-item" v-on:click="openModal('portfolio')">
          Hola
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
    margin-bottom: 64px
    margin-left: 67px
    margin-top: 7px

  .cards
    margin: 30px 67px 0 67px
    width: calc(100% - 134px)

    .portfolio-item
      display: inline-block
      width: calc(100%/3)
      background-color: yellow
  
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
