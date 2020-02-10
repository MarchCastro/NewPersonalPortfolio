<template>
  <div id="portfolioModal" v-bind:class="{active: query.modal === 'portfolio'}">
    <div v-if="query.detail === 'present'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">New Portfolio</div>
          <div class="description desktop-description">The site you're actually looking at, was designed and developed by me using
            Sketch for prototyping, Zeplin as a CSS guideline and Vue framework for the front-end development.
            <br> Please continue scrolling to find out a little bit more about me.
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/actual-portfolio.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'last'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">Old Portfolio</div>
          <div class="description desktop-description">This was used to be my last portfolio but unlike the present one,
            this one was only designed by me using a predefined template. Nevertheless, it was also helpful to practice and get started
            into the UI/UX world.
          </div>
          <div class="content-link">
            <a href="https://marcela-cf.web.app/" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/website.svg')"></div>
              <div class="subtitle desktop-link-width">Go to the site</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/last-portfolio.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'library'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">Library</div>
          <div class="description desktop-description">Online bookstore focused on showing the user an easy to use platform.
             <br> It shows the main path that a client have to follow in order to find an specific book
              with it's respective information, indicating which other actions he can do such as finding
              book descriptions and the account settings.
          </div>
          <div class="content-link">
            <a href="https://projects.invisionapp.com/share/H8U4U9O372P" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/invision.png')"></div>
              <div class="subtitle desktop-link-width">Go to the interaction</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/library.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'sapphire'">
      <div class="content">
        <div class="content-text mobile-content">
          <div class="title mobile-title">Sapphire</div>
          <div class="description mobile-description">Recommendation system with indoor location. Throughout a mobile app, mall clients 
            have the possibility to know when and where some of their favorite products may have a discount and by recommendation, 
            they can find some other products they might like. 
          </div>
          <div class="content-link">
            <div class="icon" style="backgroundImage: url('/img/portfolio-modal/play-arrow.svg')"></div>
            <div class="subtitle mobile-link-width" v-on:click="playSapphireVideo()">Play demo video</div>
          </div>
        </div>
        <div class="content-image mobile-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/sapphire.png')" v-bind:class="{hidden: playingSapphireVideo}"></div>
          <video class="sapphire" id="sapphireVideo" width="320" height="240" v-bind:class="{active: playingSapphireVideo}">
            <source src="videos/sapphire.mp4" type="video/mp4">
            Your browser does not support the video tag.
          </video> 
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'demente'">
      <div class="content">
        <div class="content-text mobile-content">
          <div class="title desktop-title">Demente</div>
          <div class="description desktop-description">Mobile app that provide students an easy way to get prepared for their 
            college/high school admission exams. 
            <br> Working as a quiz game, it throws different and previusly configured questions of a list 
            of different subjects such as chemistry, physics, etc., in order to train the students to quickly 
            think on a correct answer. 
          </div>
          <div class="content-link">
            <a href="https://projects.invisionapp.com/share/3BU4IHBW2XN#/screens" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/invision.png')"></div>
              <div class="subtitle desktop-link-width">Go to the interaction</div>
            </a>
          </div>
        </div>
        <div class="content-image mobile-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/demente.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'heartbeat'">
      <div class="content">
        <div class="content-text mobile-content">
          <div class="title desktop-title">SEEmotions!</div>
          <div class="description desktop-description">As a part of the UI/UX Specialization in Coursera and as a practical activity
            I developed the imaginary mobile app SEEmotions! which allowed young adults to monitor their heartbeat in three different stages, 
            the first one will be while they are waiting in line, the second one during the ride and finally, the third one while they are 
            descending from the roller coaster. <br> <br>
            It considered a moodboard, a pattern library and mockups.
          </div>
          <div class="content-link">
            <a href="https://drive.google.com/file/d/1_bUFxUsxYXDfg81bkhTcp5vlzGqZM3JJ/view?usp=sharing" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/list.svg')"></div>
              <div class="subtitle desktop-link-width">Explore the whole activity </div>
            </a>
          </div>
        </div>
        <div class="content-image mobile-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/Heartbeat_1.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'virgin'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">Wireframes</div>
          <div class="description desktop-description"> This visual guidance, shows the general idea of the re-design
            that Virgin Galactic is asking for, in order to get more collaborators and investors. It considers the paths
            of the user flow and the actual options that the website provides to achieve this goal, showed on the task flow diagram.
          </div>
          <div class="content-link">
            <a href="https://1drv.ms/b/s!At-_o93wWwxwqgiNw2lTx0Nysija" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/diagram.svg')"></div>
              <div class="subtitle desktop-link-width" v-on:click="playSapphireVideo()">Watch the diagram</div>
            </a>
            <a href="https://drive.google.com/file/d/1EHUNjtw1gRFTbwKG0qGztmUqkLOoP2ey/view?usp=sharing" target="_blank">
              <div class="subtitle desktop-link-width pdf" v-on:click="playSapphireVideo()">Explore the complete analysis</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/Wireframe_VG.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'virgin2'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">User Flow</div>
          <div class="description desktop-description">This user flow allows us to know which are the different and possible paths to
            do different tasks, determining the easiest and common ways to accomplish a duty.
          </div>
          <div class="content-link">
            <a href="https://1drv.ms/b/s!At-_o93wWwxwqX89PRhFiXaPtwOf" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/diagram.svg')"></div>
              <div class="subtitle desktop-link-width" v-on:click="playSapphireVideo()">Go to the interaction</div>
            </a>
            <a href="https://drive.google.com/file/d/1EHUNjtw1gRFTbwKG0qGztmUqkLOoP2ey/view?usp=sharing" target="_blank">
              <div class="subtitle desktop-link-width pdf" v-on:click="playSapphireVideo()">Explore the complete analysis</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/Mockup_VG.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'virgin3'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">Task Flow</div>
          <div class="description desktop-description">The following task flow diagram shows the way a user can become a collaborator
            within Virgin Galactic's platform. It navigates through all the possible paths that leads him to the mentioned purpose.
          </div>
          <div class="content-link">
            <a href="https://1drv.ms/b/s!At-_o93wWwxwqgMxfEp4np3M7Rit" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/diagram.svg')"></div>
              <div class="subtitle desktop-link-width" v-on:click="playSapphireVideo()">Go to the interaction</div>
            </a>
            <a href="https://drive.google.com/file/d/1EHUNjtw1gRFTbwKG0qGztmUqkLOoP2ey/view?usp=sharing" target="_blank">
              <div class="subtitle desktop-link-width pdf" v-on:click="playSapphireVideo()">Explore the complete analysis</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/Task_VG.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'library'">
      <div class="content">
        <div class="content-text desktop-content">
          <div class="title desktop-title">Sitemap </div>
          <div class="description desktop-description">Online bookstore focused on showing the user an easy to use platform.
             <br> It shows the main path that a client have to follow in order to find an specific book
              with it's respective information, indicating which other actions he can do such as finding
              book descriptions and the account settings.
          </div>
          <div class="content-link">
            <a href="https://projects.invisionapp.com/share/H8U4U9O372P" target="_blank">
              <div class="icon" style="backgroundImage: url('/img/portfolio-modal/invision.png')"></div>
              <div class="subtitle desktop-link-width">Go to the interaction</div>
            </a>
          </div>
        </div>
        <div class="content-image desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/library.png')"></div>
        </div>
      </div>
    </div>

    <!-- Education card -->
    <div v-if="query.detail === 'Coursera'">
      <div class="content">
        <div class="content-image certificates">
          <div class="image" style="backgroundImage: url('/img/certificates/calarts1.jpg')"></div>
        </div>
      </div>
    </div>
    <!-- end card -->


    <div class="close" v-on:click="closeModal()">
      <img src="../assets/img/circled_cross.svg">
    </div>
    <div class="bottom-rectangle-top"></div>
    <div class="bottom-rectangle-bottom"></div>
  </div>
</template>

<script>
import router from '@/router'

export default {
  computed: {
    query () {
      return this.$route.query
    }
  },
  data: function () {
    return {
      playingSapphireVideo: false
    }
  },
  methods: {
    closeModal () {
      router.push({ query: {} })
    },
    playSapphireVideo () {
      this.playingSapphireVideo = true
      var vid = document.getElementById('sapphireVideo')
      vid.play() 
    }
  },
  name: 'portfolioModal'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import "@/variables.sass"

  #portfolioModal
    background: #FFF
    border-radius: 4px
    height: 500px
    margin: auto 350px 
    opacity: 0
    pointer-events: none
    position: fixed
    top: 150px
    transition: all 0.3s
    vertical-align: center
    width: calc(100% - 700px)
    z-index: 10

    &.active
      opacity: 1
      pointer-events: all

    .close
      height: 20px
      position: absolute
      right: 15px
      top: 15px
      width: 20px
    
    .content
      margin: 50px 40px 50px 40px
      width: calc(100% - 80px)

      .mobile-content 
        margin: 0 10px 0 0
        width: calc(60% - 20px)
      
      .desktop-content 
        top: 0
        width: 40%

      .content-text
        display: inline-block
        height: 350px
        position: relative
        vertical-align: top

        .title
          color: #573350
          display: block
          font-family: 'CarosBold'
          font-size: 20px
          text-align: left
          text-transform: uppercase

        .mobile-title
          margin: 50px 40px 0 50px
          width: calc(100% - 100px)

        .desktop-title 
          margin: 50px 40px 0 10px
          width: calc(100% - 40px)

        .description
          color: #364252
          font-family: 'CarosLight'
          font-size: 14px
          text-align: justify
          
        .mobile-description
          margin: 15px 40px 0 50px
          width: calc(100% - 80px)

        .desktop-description
          margin: 15px 40px 0 10px
          width: calc(100% - 40px)
          
      .content-link
        cursor: pointer
        display: inline-block
        height: 50px
        margin-right: 40px
        margin-top: 30px
        opacity: .80
        position: relative
        vertical-align: top
        width: calc(100% - 32px)

        .subtitle
          color: #b75e5f
          float: right
          font-family: 'CarosLight'
          font-size: 14px
          display: inline-block
          text-align: right
          vertical-align: middle

          .mobile-link-width
            width: calc(60% - 80px)
          
          .desktop-link-width
            width: calc(60% - 40px)
          
        .pdf 
          color: #875970
          margin-top: 5px
        
        .icon
          background: no-repeat
          background-size: contain
          background-position: center
          display: inline-block
          float: right
          height: 14px
          margin-left: 8px
          margin-top: 2px
          vertical-align: middle
          width: 14px
      
      .content-image
        display: inline-block
        height: 350px
        margin: 0 10px 0 0
        position: relative
        vertical-align: top

        .image
          background: no-repeat
          background-size: contain
          background-position: center
          height: 350px
          opacity: 1
          width: calc(100%)

          &.hidden
            opacity: 0

        video.sapphire
          height: 349px
          left: 0
          opacity: 0
          position: absolute
          top: 1px
          width: 100%

          &.active
            opacity: 1

      .mobile-image 
        width: calc(40% - 20px)

      .desktop-image 
        width: calc(60% - 20px)

      .certificates
        width: 100%
              
    .bottom-rectangle-top
      background-color: #875970
      top: 450px
      height: 20px
      opacity: 0.70
      position: absolute
      width: 100%
    
    .bottom-rectangle-bottom
      background-color: #875970
      border-bottom-left-radius: 4px
      border-bottom-right-radius: 4px
      bottom: 0
      height: 35px
      position: absolute
      width: 100%


</style>
