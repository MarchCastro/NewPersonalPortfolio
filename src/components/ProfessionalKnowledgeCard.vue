<template>
  <div id="professionalKnowledgeCard" class="section">
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
          <p class="modal-text" v-on:click="openModal('certificate', 'fce')"> FCE First Certificate B2 </p>
          <p class="subtitle-card"> French </p>
          <p class="modal-text" v-on:click="openModal('certificate', 'delf')"> Delf B2 </p>
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
          <p class="content-card"> HTML/CSS </p>
          <p class="content-card"> Java </p>
          <p class="content-card"> C/C++ </p>
          <p class="subtitle-card"> Databases </p>
          <p class="content-card"> MySQL/Oracle PLSQL </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import router from '../router'
 
export default {
  methods: {
    openModal (modal, detail) {
      router.push({ path: '', query: { modal: modal, detail: detail} })
    }
  },
  name: 'ProfessionalKnowledgeCard'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  .title-page
    color: #364252
    font-family: 'CarosMedium'
    font-size: 40px
    margin-left: 67px
    margin-top: 70px
  
  .subtitle-page
    color: #364252
    font-family: 'CarosMedium'
    font-size: 18px
    margin-left: 67px
    margin-top: 7px
  
  .card-div
    margin: 30px 67px 0 67px
    width: calc(100% - 134px)
    
    .skill-card
      border-radius: 8px
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
      display: inline-block
      height: 330px
      margin-right: 56px
      vertical-align: top
      width: calc(25% - 42px)

      &:last-child
        margin-right: 0

      .top-card-rectangle
        background-color: #875970
        border-top-left-radius: 8px
        border-top-right-radius: 8px
        height: 10px
        width: 100%
    
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
  
  .modal-text
    color: #b75e5f
    cursor: pointer
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
