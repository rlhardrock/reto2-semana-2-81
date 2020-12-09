<template>
  <div id="app">
    <seccion-menu></seccion-menu>
    <seccion-banner></seccion-banner>
    <seccion-servicios></seccion-servicios>
    <seccion-footer></seccion-footer>

  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import SeccionMenu from './components/SeccionMenu.vue'
import SeccionBanner from './components/SeccionBanner.vue'
import SeccionServicios from './components/SeccionServicios.vue'
import SeccionFooter from './components/SeccionFooter.vue'


export default {
  name: 'App',
  components: {
    /* HelloWorld, */
    SeccionMenu,
    SeccionBanner,
    SeccionServicios,
    SeccionFooter
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
