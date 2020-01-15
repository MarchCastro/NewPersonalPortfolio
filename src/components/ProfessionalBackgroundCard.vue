<template>
  <div id="professionalBackgroundCard" class="section">
    <div class="card">
      
      <div class="title-page"> Professional knowledge </div>

      <div class="subtitle-page"> Here's a little bit about my professional skills </div>
      
      <div class="card-div">
        <div class="skill-card"></div>
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
    margin-left: 59px
    margin-top: 43px
    
  .skill-card
    border-radius: 8px
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
    height: 330px
    margin-right: 56px
    width: 261px
     
  @media screen and (min-width: 1440px)
    

</style>
