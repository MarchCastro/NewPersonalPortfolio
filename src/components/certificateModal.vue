<template>
  <div id="certificateModal" v-bind:class="{active: query.modal === 'certificate'}">
    <div v-if="query.detail === 'fce'">
      <div class="image" style="backgroundImage: url('/img/certificates/FCE.jpg')"></div>
    </div>

    <div v-if="query.detail === 'delf'">
      <div class="image" style="backgroundImage: url('/img/certificates/FCE.jpg')"></div>
    </div>

    <div class="close" v-on:click="closeModal()">
      <img src="../assets/img/circled_cross.svg">
    </div>
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
  name: 'certificateModal'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import "@/variables.sass"

  #certificateModal
    background: #FFF
    border-radius: 4px
    height: 700px
    margin: 0 calc(100%/2 - 500px/2)
    opacity: 0
    pointer-events: none
    position: fixed
    top: calc(100vh/2 - 700px/2)
    transition: all 0.3s
    width: 500px
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

    .image
      background: no-repeat
      background-size: contain
      background-position: center
      height: 640px
      margin: 40px 20px 20px 20px
      width: calc(100% - 40px)
    
    img 
      border: 0
</style>
