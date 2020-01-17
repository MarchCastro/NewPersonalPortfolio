<template>
  <div id="educationCard" class="section">
    <div class="card">
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
        <div class="card-subtitle"> California Institute of Arts - Coursera </div>
        <div class="card-subtitle"> Université de Technologie de Compiègne </div>
        <div class="card-subtitle"> Escuela Superior de Cómputo </div>
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
    margin-top: 64px

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
  
  
</style>
