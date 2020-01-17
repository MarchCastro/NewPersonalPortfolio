<template>
  <div id="professionalBackgroundCard" class="section">
    <div class="card">
      
      <div class="title-page"> Professional knowledge </div>

      <div class="subtitle-page"> Here's a little bit about my professional skills </div>
      
      
      <div class="card-div">
        <!--Languages card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/languages.png">
          <div class="title-card-div">
            <p class="title-card"> Languages </p>
          </div>
          <p class="subtitle-card"> Spanish </p>
          <p class="content-card"> Native </p>
          <p class="subtitle-card"> English </p>
          <p class="content-card"> FCE First Certificate B2 </p>
          <p class="subtitle-card"> French </p>
          <p class="content-card"> Delf B2 </p>
        </div>

        <!--Technologies card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/technologies.png">
          <div class="title-card-div">
            <p class="title-card"> Technologies </p>
          </div>
          <p class="subtitle-card"> Design tools </p>
          <p class="content-card"> Sketch </p>
          <p class="content-card"> Adobe XD </p>
          <p class="content-card"> inVision </p>
          <p class="content-card"> Zeplin </p>
        </div>

        <!--Skills card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/skills1.png">
          <div class="title-card-div">
            <p class="title-card"> Skills </p>
          </div>
          <p class="content-card"> Wireframing </p>
          <p class="content-card"> User/Task Flow Design </p>
          <p class="content-card"> Interaction Map Design </p>
          <p class="content-card"> Sitemap Design </p>
          <p class="content-card"> Mobile Interface Design </p>
        </div>
        <!--Tools card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/code1.png">
          <div class="title-card-div">
            <p class="title-card"> Dev. tools </p>
          </div>
          <p class="subtitle-card"> Dev. Languages </p>
          <p class="content-card"> Java </p>
          <p class="content-card"> C/C++ </p>
          <p class="subtitle-card"> Databases </p>
          <p class="content-card"> MySQL/Oracle PLSQL </p>
        </div>
      </div>

      <!-- Slider options -->
      <div class="slider-options">
        <img class="actual-slider" src="../assets/img/actual-option@3x.png">
        
        <hr class="hr">
        
        <a href="#section-aboutme2">
          <img class="second-slider" src="../assets/img/second-option@3x.png">
        </a>
      </div>
      <div class="slider-text-div">
        <p class="actual-slider-text"> Who am I? </p>
        <p class="second-slider-text"> Professional Background </p>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'ProfessionalBackgroundCard'
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
  
  .card-div
    margin-left: 50px
    margin-top: 43px
    
  .skill-card
    border-radius: 8px
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
    display: inline-block
    height: 330px
    margin: 25px
    width: 261px
    
  .top-card-rectangle
    background-color: #875970
    border-top-left-radius: 8px
    border-top-right-radius: 8px
    height: 10px
    width: 261px 
    
  
  .card-icon  
    height: 72px
    margin-left: 95px
    margin-top: 38px
    width: 72px
  
  .title-card-div
    margin-top: 10px
    text-align: center
    width: auto

  .title-card
    color: #364252
    font-family: 'CarosMedium'
    font-size: 18px

  .subtitle-card
    color: #364252
    font-family: 'CarosMedium'
    font-size: 15px
    line-height: 0px
    margin-left: 43px
    margin-top: 15px
    text-align: left
  
  .content-card
    color: #364252
    font-family: 'CarosLight'
    font-size: 13px
    margin-left: 43px
    text-align: left
  
  .slider-options
    display: inline-flex
    margin-left: 851px
    margin-top: 20px
    vertical-align: middle
  
  .actual-slider
    height: 38px
    width: 38px
  
  .second-slider  
    height: 29px
    margin-right: 232px
    margin-top: 10px
    width: 29px

  .hr
    border-top: dotted 5px
    height: 1px
    margin-top: 20px
    width: 180px
  
  .slider-text-div 
    display: flex
    height: 18px
    margin-top: 8px
  
  .actual-slider-text
    color: #364252
    font-family: 'CarosMedium'
    font-size: 15px
    margin-left: 831px
    
  .second-slider-text
    color: #364252
    font-family: 'CarosMedium'
    font-size: 15px
    margin-left: 80px
    margin-right: 164px


  @media screen and (min-width: 1440px)
    

</style>
