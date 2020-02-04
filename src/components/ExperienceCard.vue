<template>
  <div id="experienceCard" class="section">
    <div class="card">
       <!-- Decoration ovals -->
      <div class="oval one purple-three"></div>
      <div class="oval two purple-two"></div>
      <div class="oval three purple-one"></div>
      <div class="oval four purple-four"></div>
      <div class="oval five purple-one"></div>
      <div class="oval six purple-two"></div>
      <div class="oval seven purple-four"></div>

      <!-- Title page -->
      <div class="title-page"> Where have I worked? </div>
      <div class="subtitle-page"> This is the experience I've gained. </div>

      <!-- Cards-->
      <div class="cards">
        <!-- Freelance card -->
        <div class="card-item" v-bind:class="{'open': cards.first.open}">
          <div class="experience-item">
            <div class="image" style="backgroundImage:url('img/experience-img/Freelance.png')"></div>

            <div class="title"> Freelancer </div>
            <div class="date"> Jan 2019 - Present </div>

            <div class="content">Recommendation system with indoor location.</div>

            <img class="arrow" v-on:click="cards.first.open = !cards.first.open" src="../assets/img/arrow_experience.png">
          
          </div>
          
          <div class="card">
            <div class="title-card">Activities and tools</div>
            <div class="content-card"> Adobe XD, Sketch, inVision, Zeplin, Illustrator. </div>
            <div class="bottom-card-rectangle"></div>
          </div>
        </div>

        <!-- Business Analyst card -->
        <div class="card-item" v-bind:class="{'open': cards.second.open}">
          <div class="experience-item">
            <a href="https://www.netlogistik.com/es/" target="_blank"> 
              <div class="image" style="backgroundImage:url('img/experience-img/netlogistik.png')"></div>
            </a>

            <div class="title"> Business Analyst </div>
            <div class="date"> Jan 2019 - Present </div>

            <div class="content"> Business analysis focused on supply’s chain logistics software. </div>

            <img class="arrow" v-on:click="cards.second.open = !cards.second.open" src="../assets/img/arrow_experience.png">
            
          </div>
        
          <div class="card">
            <div class="title-card">Activities and tools</div>
            <div class="content-card"> Epics, User stories, User's handbooks, SCRUM, Documentation, Client requirements, Activities planning and priorization, Team management.  </div>
            <div class="bottom-card-rectangle"></div>
          </div>
        </div>

        <!-- Internship card -->
        <div class="card-item" v-bind:class="{'open': cards.third.open}">
          <div class="experience-item">
            <a href="https://www.gob.mx/imp" target="_blank"> 
              <div class="image" style="backgroundImage:url('img/experience-img/imp.png')"></div>
            </a>

            <div class="title"> Internship </div>
            <div class="date"> Feb 2018 - Aug 2018 </div>

            <div class="content">Processes simulation system for the National Refination System plants of PEMEX to certificate plant operators.</div>

            <img class="arrow" v-on:click="cards.third.open = !cards.third.open" src="../assets/img/arrow_experience.png">

            <div class="bottom-card-rectangle"></div>
          </div>

          <div class="card">
            <div class="title-card">Activities and tools</div>
            <div class="content-card"> HMIWeb Display Builder by Honeywell, User Interfaces Design, C#, Project documentation. </div>
            <div class="bottom-card-rectangle"></div>
          </div>
        </div>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      cards: {
        first: {
          open: false
        },
        second: {
          open: false
        },
        third: {
          open: false
        }
      }
    }
  },
  name: 'ExperienceCard'
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

  .cards
    margin: 30px 80px 0 80px
    width: calc(100% - 160px)

    .card-item
      border-radius: 8px
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5)
      display: inline-block
      height: 353px
      margin-right: 60px
      position: relative
      transition: all 0.3s
      vertical-align: top 
      width: calc(100%/3 - 40px)

      &:last-child
        margin-right: 0

      .experience-item
        background: #FFF
        border-radius: 0 0 8px 8px
        height: 313px
        position: relative
        z-index: 2

        .image
          background-position: center
          background-repeat: no-repeat
          background-size: contain
          height: 75px
          margin: 30px 50px
          vertical-align: middle
          width: calc(100% - 100px)

        .title
          color: #364252
          font-family: 'CarosBold'
          font-size: 23px
          text-align: center
          width: 100%
        
        .date
          color: #364252
          font-family: 'CarosLight'
          font-size: 13px
          margin-top: 5px
          margin-bottom: 25px
          opacity: 0.65
          text-align: center
          width: 100%

        .content
          color: #364252
          font-family: 'CarosLight'
          font-size: 15px
          margin-bottom: 25px
          padding: 0 37px
          text-align: center
          width: calc(100% - 74px)
        
        .arrow
          bottom: 35px
          cursor: pointer
          height: 13px
          margin: 0 calc(50% - 12px)
          position: absolute
          transition: all 0.3s
          width: 28px

      .card
        background-color: #FFF
        border-bottom-left-radius: 8px
        border-bottom-right-radius: 8px
        border-top-left-radius: 0
        border-top-right-radius: 0
        border-style: hidden
        bottom: 0
        height: 135px
        margin: 0
        position: absolute
        width: 100%
        z-index: 0    

        .title-card
          font-family: 'CarosMedium'
          font-size: 15px
          margin-top: 18px
          text-align: center
          width: 100%
        
        .content-card
          font-family: 'CarosLight'
          font-size: 13px
          margin-top: 10px
          padding: 0 37px
          text-align: justify
          width: calc(100% - 74px)

        .bottom-card-rectangle
          background-color: #b75e5f
          bottom: 0
          border-bottom-left-radius: 8px
          border-bottom-right-radius: 8px
          height: 10px
          opacity: 0.75
          position: absolute
          width: 100%
    
      &.open
        height: 460px
        img.arrow
          transform: rotate3d(0, 0, 1, 180deg)
    
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
        height: 11px
        left: 1250px
        top: 30px
        width: 11px

      &.two
        height: 31px
        left: 1156px
        top: 51px
        width: 31px

      &.three
        height: 23px
        left: 1277px
        top: 74px
        width: 23px

      &.four
        height: 74px
        left: 1197px
        top: 74px
        width: 74px

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
</style>
