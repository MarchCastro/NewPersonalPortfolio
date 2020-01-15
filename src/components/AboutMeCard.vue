<template>
  <div id="aboutMeCard" class="section">
    <div class="card">
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

      <button class="button-cv">Download CV</button>

    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMeCard'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  .oval
    border-radius: 50%
    position: absolute

    &.purple-one
      background: #843b62

    &.purple-two
      background:  #74546a

    &.purple-three
      background: #6d435a

    &.purple-four
      background: #352d39

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
    margin-top: 116px
    width: 165px
  
  .button-cv:hover
    background-color: #fff
    color: #b75e5f
    border: 2px solid #b75e5f

  .passion-icon-div 
    margin-left: 597px
    margin-top: 29px

  .passion-icon
    height: 41px    
    margin-right: 16px
    width: 41px
    
    
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
