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
        <div class="card-item">
          <div class="experience-item">
            <a href="https://www.coursera.org/specializations/ui-ux-design" target="_blank"> 
              <img class="image" src="../assets/img/CIA.png">
            </a>

            <div class="title"> Freelance </div>
            <div class="date"> Jan 2019 - Present </div>

            <div class="content">Recommendation system with indoor location.</div>

          </div>
          <div class="card">
              <div class="title-card">Activities and tools</div>
              <div class="content-card"> Adobe XD, Sketch, inVision, Zeplin, Illustrator. </div>
          </div>
        </div>

        <!-- Freelance card -->
        <div class="card-item">
          <div class="experience-item">
            <a href="https://www.coursera.org/specializations/ui-ux-design" target="_blank"> 
              <img class="image" src="../assets/img/CIA.png">
            </a>

            <div class="title"> Freelance </div>
            <div class="date"> Jan 2019 - Present </div>

            <div class="content">Recommendation system with indoor location.</div>

          </div>
          <div class="card">
              <div class="title-card">Activities and tools</div>
              <div class="content-card"> Adobe XD, Sketch, inVision, Zeplin, Illustrator. </div>
          </div>
        </div>

        <!-- Freelance card -->
        <div class="card-item">
          <div class="experience-item">
            <a href="https://www.coursera.org/specializations/ui-ux-design" target="_blank"> 
              <img class="image" src="../assets/img/CIA.png">
            </a>

            <div class="title"> Freelance </div>
            <div class="date"> Jan 2019 - Present </div>

            <div class="content">Recommendation system with indoor location.</div>

          </div>
          <div class="card">
              <div class="title-card">Activities and tools</div>
              <div class="content-card"> Adobe XD, Sketch, inVision, Zeplin, Illustrator. </div>
          </div>
        </div>

          
        
        


      </div>

    </div>
  </div>
</template>

<script>
export default {
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
    margin-top: 7px

  .cards
    margin: 30px 67px 0 67px
    width: calc(100% - 134px)

    .card-item
      display: inline-block
      height: 395px
      width: calc(100%/3)

    .experience-item
      border: 1.5px solid rgba(63.05%, 26.76%, 11.01%, 0.75)
      border-top-left-radius: 8px
      border-top-right-radius: 8px
      height: 268px

      .image
        border-radius: 4px
        display: inline
        height: 84px
        margin: 20px 80px 30px 80px
        vertical-align: middle
        width: calc(100% - 230px)

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
        margin-bottom: 15px
        opacity: 0.65
        text-align: center
        width: 100%

      .content
        color: #364252
        font-family: 'CarosLight'
        font-size: 16px
        margin-bottom: 22px
        text-align: center
        width: 100%

    .card
      background-color: #b75e5f
      border-bottom-left-radius: 8px
      border-bottom-right-radius: 8px
      border-top-left-radius: 0
      border-top-right-radius: 0
      border-style: hidden
      height: 127px
      margin:0
      opacity: 0.75
      width: 100%

      .title-card
        color: #fff
        font-family: 'CarosMedium'
        font-size: 15px
        margin-top: 22px
        text-align: center
        width: 100%
      
      .content-card 
        color: #fff
        font-family: 'CarosLight'
        font-size: 13px
        margin-top: 10px
        text-align: center
        width: 100%

        
  
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
