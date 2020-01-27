<template>
  <div id="portfolioModal" v-bind:class="{active: query.modal === 'portfolio'}">
    portfolioModal
  </div>
</template>

<script>
export default {
  computed: {
    query () {
      return this.$route.query
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
    height: 400px
    left: calc(50vw - 200px)
    opacity: 0
    pointer-events: none
    position: fixed
    top: 200px
    transition: all 0.3s
    width: 400px
    z-index: 10

    &.active
      opacity: 1
      pointer-events: all

</style>
