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
        </div>
        <!--Technologies card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/technologies.png">
        </div>
        <!--Skills card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/skills1.png">
        </div>
        <!--Tools card -->
        <div class="skill-card">
          <div class="top-card-rectangle"></div>
          <img class="card-icon" src="../assets/img/code1.png">
        </div>
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
    height: 330px
    margin: 25px
    width: 261px
    display: inline-block
  
  .top-card-rectangle
    background-color: #875970
    height: 10px
    width: 261px 
    border-top-right-radius: 8px
    border-top-left-radius: 8px
  
  .card-icon  
    height: 72px
    margin-left: 95px
    margin-top: 38px
    width: 72px


  @media screen and (min-width: 1440px)
    

</style>
