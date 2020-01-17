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
      
      <!-- Cards title -->
      <div class="card-title-div">
        <div class="card-title"> UI/UX Specialization </div>
        <div class="card-title"> Exchange Program </div>
        <div class="card-title"> Bachelor's Degree </div>
      </div>

      <!-- Cards subtitle --> 
      <div class="card-subtitle-div">  
        <a href="https://www.coursera.org/specializations/ui-ux-design" class="card-subtitle" target="_blank"> California Institute of Arts - Coursera </a>
        <a href="https://www.utc.fr/" class="card-subtitle" target="_blank"> Université de Technologie de Compiègne </a>
        <a href="http://www.escom.ipn.mx/" class="card-subtitle" target="_blank"> Escuela Superior de Cómputo </a>
      </div>
      <!-- Cards-->
      <div class="card-div">
        <!--CIA card -->
        <div class="education-card">
          <img class="image" src="../assets/img/CIA.png">
          <div class="overlay">
            <div class="text">Hello World</div>
          </div>
        </div>
        
        
        <!--UTC card -->
        <img class="education-card" src="../assets/img/UTC.png">
        <!--ESCOM card -->
        <img class="education-card" src="../assets/img/ESCOM.png">
      </div>

      <!-- Cards date --> 
      <div class="card-date-div">
        <div class="card-date"> 2019 - Present </div>
        <div class="card-date"> 2017 - 2018 </div>
        <div class="card-date"> 2014 - 2019 </div>
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
    margin-left: 67px
    margin-top: 7px
  
  .card-title-div
    display: flex
    height: 28px
    margin-left: 65px
    margin-right: 65px
    margin-top: 30px

  .card-title
    color: #364252
    font-family: 'CarosBold'
    font-size: 23px
    margin: 30px
    text-align: center
    width: 369px
  
  .card-subtitle-div
    display: flex
    height: 21px
    margin-left: 65px
    margin-right: 65px
    margin-top: 13px

  .card-subtitle
    color: #b75e5f
    font-family: 'CarosMedium'
    font-size: 18px
    margin: 19px
    text-align: center
    text-decoration: none
    width: 369px
  
  .card-date-div
    display: flex
    margin-left: 65px
    margin-right: 65px
    vertical-align: middle

  .card-date
    color: #364252
    font-family: 'CarosLight'
    font-size: 15px
    margin: 0 19px 0 19px
    opacity: 0.65
    text-align: right
    width: 369px

  .card-div
    margin-left: 65px
    margin-right:65px
    margin-top: 21px
    
  .education-card
    border-radius: 4px
    border-style: hidden
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
    height: 265px
    margin: 17px
    width: 369px
    display: inline-block
  
  .image 
    display: block
    width: 100%
    height: auto
  
  .overlay 
    position: absolute
    bottom: 0
    left: 0
    right: 0
    background-color: #008CBA
    overflow: hidden
    width: 100%
    height: 0
    transition: .5s ease
  
  .education-card:hover .overlay 
    height: 100%
  
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
