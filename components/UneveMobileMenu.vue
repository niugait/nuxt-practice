<template>
    <div>
      <nav role="navigation">
        <div id="uneve-mobile-menu">
          <input type="checkbox" @change="clicked = !clicked"/>
          <span></span>
          <span></span>
          <span></span>
          <ul id="uneve-mobile-menu-list" v-if="clicked">
            <a href="#"><li>Início</li></a>
            <a href="#"><li>Uneve</li></a>
            <a href="#"><li>Benefícios</li></a>
            <a href="#"><li>Blog</li></a>
          </ul>
        </div>
      </nav>
    </div>
</template>

<script>
    export default {
        name: "UneveMobileMenu",
      data() {
          return {
            clicked: false
          }
      }
    }
</script>

<style scoped lang="sass">
#uneve-mobile-menu
  display: block
  position: absolute
  z-index: 1
  -webkit-user-select: none
  user-select: none

#uneve-mobile-menu input
  display: block
  width: 40px
  height: 32px
  position: absolute
  top: -7px
  left: -5px
  cursor: pointer
  opacity: 0 /* hide this */
  z-index: 2 /* and place it over the hamburger */
  -webkit-touch-callout: none

#uneve-mobile-menu span
  display: block
  width: 33px
  height: 4px
  margin-bottom: 5px
  position: relative

  background: #fff
  border-radius: 3px

  z-index: 1
  transform-origin: 4px 0px
  transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0), background 0.5s cubic-bezier(0.77,0.2,0.05,1.0), opacity 0.55s ease

#uneve-mobile-menu span:first-child
  transform-origin: 0 0

#uneve-mobile-menu span:nth-last-child(2)
  transform-origin: 0 100%

#uneve-mobile-menu input:checked ~ span
  opacity: 1
  transform: rotate(45deg) translate(-2px, -1px)
  background: #232323

#uneve-mobile-menu input:checked ~ span:nth-last-child(3)
  opacity: 0
  transform: rotate(0deg) scale(0.2, 0.2)

#uneve-mobile-menu input:checked ~ span:nth-last-child(2)
  transform: rotate(-45deg) translate(0, -1px)

#uneve-mobile-menu input:checked ~ ul
  transform: none
</style>
