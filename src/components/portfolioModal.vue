<template>
  <div id="portfolioModal" v-bind:class="{active: query.modal === 'portfolio'}">
    <div v-if="query.detail === 'last'">
      last
    </div>

    <div v-if="query.detail === 'library'">
      library
    </div>

    <div v-if="query.detail === 'sapphire'">
      <div class="content">
        <div class="content-text">
          <div class="title">Sapphire</div>
          <div class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
        </div>
        <div class="content-text">
          <div class="image" style="backgroundImage: url('/img/UserFlow_VG.png')"></div>
        </div>
      </div>
    </div>

    <div v-if="query.detail === 'demente'">
      demente
    </div>

    <div class="close" v-on:click="closeModal()">
      <img src="../assets/img/circled_cross.svg">
    </div>
    <div class="bottom_rectangle"></div>
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
  methods: {
    closeModal () {
      router.push({ query: {} })
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
      margin: 70px 40px 70px 40px
      width: calc(100% - 80px)
    
      .content-text
        display: inline-block
        height: 350px
        margin: 0 10px 0 0
        position: relative
        vertical-align: top
        width: calc(100%/2 - 20px)

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
        
        .image
          background: no-repeat
          background-size: contain
          background-position: center
          height: 640px
          margin: 0 20px 
          width: calc(100% - 40px)
      
    .bottom_rectangle
      background-color: #875970
      border-bottom-left-radius: 4px
      border-bottom-right-radius: 4px
      height: 60px
      opacity: 0.90
      width: auto


</style>
