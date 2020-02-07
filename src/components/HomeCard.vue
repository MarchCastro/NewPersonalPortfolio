<template>
  <div id="homeCard" class="section">
    <div class="card">
      
      <!-- ovals -->
      <div class="oval one purple-two"></div>
      <div class="oval two purple-two"></div>
      <div class="oval three purple-one"></div>
      <div class="oval four purple-one"></div>
      <div class="oval five purple-two"></div>
      <div class="oval six purple-one"></div>
      <div class="oval seven purple-one"></div>
      <div class="oval eight purple-three"></div>
      <div class="oval nine purple-two"></div>
      <div class="oval ten purple-four"></div>
      <div class="oval eleven purple-two"></div>
      <div class="oval twelve purple-one"></div>
      <div class="oval thirteen purple-two"></div>
      <div class="oval fourteen purple-four"></div>
      <div class="oval fifteen purple-one"></div>
      <div class="oval sixteen purple-two"></div>
      <!-- end ovals -->

      <div class="name"> Marcela <br> Castro Flores </div>

      <div class="job"> UI/UX Designer </div>

      <img class="profile-picture" src="../assets/img/me-picture@3x.png">

      <div class="follow-me">
        <span> Follow me </span>
        <img class="arrow" src="../assets/img/arrow.svg">
        
        <a class="linkedin" href="https://linkedin.com/in/marcela-castro-flores" target="_blank">
          <img src="../assets/img/linkedin-border.svg">
          <img src="../assets/img/linkedin-border-hover.svg" class="hover">
        </a>

        <a class="angelist" href="https://angel.co/marcela-castro-flores" target="_blank">
          <img src="../assets/img/angelist.svg">
          <img src="../assets/img/angelist-hover.svg" class="hover">
        </a>
        
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeCard'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import "@/variables.sass"
  
  .oval
    border-radius: 50%
    position: absolute

    &.one

    &.two

    &.three

    &.four

    &.five

    &.six

    &.seven

    &.eight

    &.nine

    &.ten

    &.eleven

    &.twelve

    &.purple-one
      background: $purple-one

    &.purple-two
      background: $purple-two

    &.purple-three
      background: $purple-three

    &.purple-four
      background: $purple-four
  
  .name
    color: #b75e5f
    font-family: 'CarosBold'
    font-size: 50px
    margin-left: 202px
    margin-top: 260px
  
  .job
    color: #364252
    font-family: 'CarosMedium'
    font-size: 40px
    margin-left: 202px
    margin-top: 60px

  .profile-picture
    height: 371px
    left: 758px
    position: absolute
    top: 177px
    width: 371px

  .follow-me
    color: #364252
    font-family: 'CarosBold'
    font-size: 15px
    left: -30px
    line-height: 40px
    position: absolute
    top: 350px
    transform: rotate3d(0, 0, 1, 270deg)
    
    a
      display: inline-block
      vertical-align: top

    img
      transform: rotate3d(0, 0, 1, 90deg)
      vertical-align: middle

    .arrow
      height: 22xpx
      margin-left: 40px
      width: 13px

    .linkedin
      margin-left: 43px
      margin-right: 40px
      position: relative
      
      img
        height: 23px
        margin-top: 10px
        position: absolute
        width: 25px

        &.hover
          opacity: 0

      &:hover
        img.hover
          opacity: 1

    .angelist
      margin-right: 19px
      position: relative

      img
        height: 23px  
        margin-top: 10px
        position: absolute
        width: 25px

        &.hover
          opacity: 0

      &:hover
        img.hover
          opacity: 1

  @media screen and (min-width: 576px)

  @media screen and (min-width: 576px)

  @media screen and (min-width: 1438px)
    .oval
      &.one
        height: 15px
        left: 45px
        top: 45px
        width: 15px

      &.two
        height: 27px
        left: 178px
        top: 26px
        width: 27px

      &.three
        height: 80px
        left: 64px
        top: 97px
        width: 80px

      &.four
        height: 65px
        left: 712px
        top: 144px
        width: 65px

      &.five
        height: 15px
        left: 912px
        top: 129px
        width: 15px

      &.six
        height: 235px
        left: 1031px
        top: 115px
        width: 235px

      &.seven
        height: 235px
        left: 1031px
        top: 115px
        width: 235px

      &.eight
        height: 152px
        left: 671px
        top: 347px
        width: 152px

      &.nine
        height: 53px
        left: 1221px
        top: 422px
        width: 53px

      &.ten
        height: 198px
        left: 1000px
        top: 415px
        width: 198px

      &.eleven
        height: 15px
        left: 144px
        top: 541px
        width: 15px

      &.twelve
        height: 15px
        left: 37px
        top: 614px
        width: 15px

      &.thirteen
        height: 27px
        left: 128px
        top: 641px
        width: 27px

      &.fourteen
        height: 107px
        left: 805px
        top: 562px
        width: 107px

      &.fifteen
        height: 41px
        left: 1000px
        top: 647px
        width: 41px

      &.sixteen
        height: 15px
        left: 1206px
        top: 668px
        width: 15px

</style>
