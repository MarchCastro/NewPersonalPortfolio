<template>
  <div id="educationCard" class="section">
    <div class="card">
      <!-- Decoration ovals -->
      <div class="oval one purple-one"></div>
      <div class="oval two purple-four"></div>
      <div class="oval three purple-three"></div>
      <div class="oval four purple-two"></div>
      <div class="oval five purple-one"></div>
      <div class="oval six purple-two"></div>
      <div class="oval seven purple-four"></div>

      <!-- Title page -->
      <div class="title-page"> Education </div>
      <div class="subtitle-page"> Here, you can find the places where I've learned. </div>

      <!-- Cards-->
      <div class="cards">
        <!--CIA card -->
        <div class="education-item">
          <div class="title"> UI/UX Specialization </div>
          <a href="https://www.coursera.org/specializations/ui-ux-design" class="subtitle" target="_blank"> California Institute of Arts - Coursera </a>
          
          <div class="card">
            <img class="image" src="../assets/img/CIA.png">
            <div class="overlay">
              <a href="www.facebook.com" target="_blank" class="text-overlay"> Visual Elements of User Interface Design </a>
            </div>
          </div>
          
          <div class="date"> 2019 - Present </div>
        </div>

        <!--UTC card -->
        <div class="education-item">
          <div class="title"> Exchange Program </div>
          <a href="https://www.utc.fr/" class="subtitle" target="_blank"> Université de Technologie de Compiègne </a>
          
          <div class="card">
            <img class="image" src="../assets/img/UTC.png">
            <div class="overlay">
              <a href="www.facebook.com" target="_blank" class="text-overlay"> Informatic Engineering </a>
            </div>
          </div>

          <div class="date"> 2017 - 2018 </div>
        </div>

        <!--ESCOM card -->
        <div class="education-item">
          <div class="title"> Bachelor's Degree </div>
          <a href="http://www.escom.ipn.mx/" class="subtitle" target="_blank"> Escuela Superior de Cómputo </a>
          
          <div class="card">
            <img class="image" src="../assets/img/ESCOM.png"> 
            <div class="overlay">
              <a href="www.facebook.com" target="_blank" class="text-overlay"> Computing Systems Engineering </a>
            </div>
          </div>

          <div class="date"> 2014 - 2019 </div>
        </div>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'EducationCard'
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

    .education-item
      display: inline-block
      width: calc(100%/3)

      .title
        color: #364252
        font-family: 'CarosBold'
        font-size: 23px
        text-align: center
        width: 100%

      .subtitle
        color: #b75e5f
        display: block
        font-family: 'CarosMedium'
        font-size: 18px
        margin-bottom: 22px
        text-align: center
        text-decoration: none
        width: 100%

      .card
        border-radius: 4px
        border-style: hidden
        box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
        display: inline-block
        height: 265px
        margin: 0 17px
        position: relative
        width: calc(100% - 34px)

        .image
          border-radius: 4px
          display: block
          height: 274px
          margin: -4px 0 0 -8px
          min-width: calc(100% + 16px)

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
          height: 30%

      .date
        color: #364252
        font-family: 'CarosLight'
        font-size: 15px
        margin-right: 17px
        margin-top: 11px
        opacity: 0.65
        text-align: right
        width: calc(100% - 17px)

  .card-div
    margin-left: 65px
    margin-right:65px
    margin-top: 21px
  
  
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
        height: 18px
        left: 1201px
        top: 70px
        width: 18px

      &.two
        height: 60px
        left: 1225px
        top: 30px
        width: 60px

      &.three
        height: 9px
        left: 1270px
        top: 100px
        width: 9px

      &.four
        height: 25px
        left: 1290px
        top: 90px
        width: 25px

      &.five
        height: 14px
        left: 22px
        top: 627px
        width: 14px

      &.six
        height: 45px
        left: 13px
        top: 678px
        width: 45px

      &.seven
        height: 22px
        left: 62px
        top: 666px
        width: 22px
  
</style>
