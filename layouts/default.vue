<template>
  <div class="page">
    <div class="uneve-header">
      <div class="uneve-header-section">
        <div class="uneve-header-logo">
          <uneve-logo />
        </div>
        <div v-if="screenSize > 768">
          <div class="uneve-header-menu">
            <a href="#">Início</a>
            <a href="#">Uneve</a>
            <a href="#">Benefícios</a>
            <a href="#">Blog</a>
          </div>
        </div>
        <div v-else>
          <uneve-mobile-menu />
        </div>
      </div>
      <div class="uneve-header-section">
        <div class="uneve-spacer-160"></div>
      </div>
    </div>
    <div class="uneve-white-box">
      <nuxt />
    </div>
  </div>
</template>

<script>
  import UneveLogo from '~/components/UneveLogo.vue'
  import UneveMobileMenu from '~/components/UneveMobileMenu.vue'

  export default {
    components: {
      UneveLogo,
      UneveMobileMenu
    },
    head () {
      return {
        link: [
          { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css?family=Poppins&display=swap' }
        ]
      }
    },
    computed: {
      screenSize: function () {
        return screen.width;
      }
    }
  }
</script>

<style lang="sass">
$primary-color: #01C0C8
$side-spacer: 160px

.uneve-header
  background-color: $primary-color

.uneve-header-section
  max-height: 160px
  display: flex
  margin: 0 auto
  align-items: center
  max-width: 1110px
  justify-content: space-between

.uneve-header-menu
  padding: 68px 0

.uneve-header-menu a
  color: #fff
  margin-left: 24px
  font-size: 16px
  line-height: 24px

.uneve-spacer-160
  height: 160px

.uneve-white-box
  margin: -160px auto 80px
  background-color: #fff
  padding: 80px
  max-width: 1110px
  box-shadow: 4px 4px 32px rgba(76, 87, 89, 0.08)
  border-radius: 0 0 48px 48px

a
  text-decoration: none

html
  background-color: #E8ECED
*,
*:before,
*:after
  box-sizing: border-box
  margin: 0
  font-family: 'Poppins', sans-serif

@media (min-width: 1024px)
  .uneve-white-box,
  .uneve-header-section
    max-width: 976px

@media (max-width: 768px)
  .uneve-white-box,
  .uneve-header-section
    padding: 40px 20px

</style>
