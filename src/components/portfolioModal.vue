<template>
  <div id="portfolioModal" v-bind:class="{active: query.modal === 'portfolio'}">
    <div v-if="query.detail === 'last'">
      <div class="content">
        <div class="content-desktop-text">
          <div class="title">Old Portfolio</div>
          <div class="description"> This used to be my old portfolio. Unlike the one you're looking at, this one was
            only designed by 
          </div>
          <div class="content-link">
            <div class="subtitle">Play demo video</div>
            <div class="icon" style="backgroundImage: url('/img/portfolio-modal/play-arrow.svg')"></div>
          </div>
        </div>
        <div class="content-desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/library.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'library'">
      <div class="content">
        <div class="content-desktop-text">
          <div class="title">Library</div>
          <div class="description">Online bookstore focused on showing the user an easy to use platform.
             It shows the main path that a client have to follow in order to find an specific book
              with it's respective information, indicating which other actions he can do such as finding
              book descriptions and the account settings.
          </div>
          <div class="content-link">
            <div class="subtitle">Play demo video</div>
            <div class="icon" style="backgroundImage: url('/img/portfolio-modal/play-arrow.svg')"></div>
          </div>
        </div>
        <div class="content-desktop-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/library.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'sapphire'">
      <div class="content">
        <div class="content-mobile-text">
          <div class="title">Sapphire</div>
          <div class="description">Recommendation system with indoor location. Throughout a mobile app, mall clients 
            have the possibility to know when and where some of their favorite products may have a discount and by recommendation, 
            they can find some other products they might like. 
          </div>
          <div class="content-link">
            <div class="icon" style="backgroundImage: url('/img/portfolio-modal/play-arrow.svg')"></div>
            <div class="subtitle" v-on:click="playSapphireVideo()">Play demo video</div>
          </div>
        </div>
        <div class="content-mobile-image">
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
        <div class="content-mobile-text">
          <div class="title">Demente</div>
          <div class="description">Mobile app to help people change the way they study for their college/high school admission exams.  
          </div>
          <div class="content-link">
            <div class="subtitle">Play demo video</div>
            <div class="icon" style="backgroundImage: url('/img/portfolio-modal/play-arrow.svg')"></div>
          </div>
        </div>  
        <div class="content-mobile-image">
          <div class="image" style="backgroundImage: url('/img/portfolio-modal/demente.png')"></div>
        </div>
      </div>
    </div>

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
    
      .content-mobile-text
        display: inline-block
        height: 350px
        margin: 0 10px 0 0
        position: relative
        vertical-align: top
        width: calc(60% - 20px)

        .title
          color: #573350
          display: block
          font-family: 'CarosBold'
          font-size: 20px
          margin: 50px 40px 0 50px
          text-align: left
          text-transform: uppercase
          width: calc(100% - 100px)
        
        .description
          color: #364252
          font-family: 'CarosLight'
          font-size: 14px
          margin: 15px 40px 0 50px
          text-align: justify
          width: calc(100% - 80px)
        
        .content-link
          display: inline-block
          height: 50px
          margin-right: 40px
          margin-top: 50px
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
            width: calc(60% - 80px)
          
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
      
      .content-mobile-image
        display: inline-block
        height: 350px
        margin: 0 10px 0 0
        position: relative
        vertical-align: top
        width: calc(40% - 20px)

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
      
      .content-desktop-text
        display: inline-block
        height: 350px
        position: relative
        vertical-align: top
        width: 40%

        .title
          color: #573350
          display: block
          font-family: 'CarosBold'
          font-size: 20px
          margin: 50px 0 0 10px
          text-align: left
          text-transform: uppercase
          width: calc(100% - 40px)
        
        .description
          color: #364252
          font-family: 'CarosLight'
          font-size: 12px
          margin: 15px 40px 0 10px
          text-align: justify
          width: calc(100% - 40px)
        
        .content-link
          display: inline-block
          height: 50px
          position: relative
          vertical-align: top
          width: 100%

          .subtitle
            color: #364252
            font-family: 'CarosLight'
            font-size: 10px
            margin: 15px 40px 0 50px
            vertical-align: middle
            text-align: right
          
          .icon
            background: no-repeat
            background-size: contain
            background-position: center
            height: 20px
            vertical-align: middle
            width: 20px
      
      .content-desktop-image
        display: inline-block
        height: 350px
        margin: 0 10px 0 0
        position: relative
        vertical-align: top
        width: calc(60% - 20px)

        .image
          background: no-repeat
          background-size: contain
          background-position: center
          height: 350px
          width: calc(100%)
      
    .bottom-rectangle-top
      background-color: #875970
      top: 440px
      height: 30px
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
