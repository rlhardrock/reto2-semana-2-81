<template>
  <div id="app">
    <seccion-menu></seccion-menu>
        <seccion-banner></seccion-banner>
    <br>
    <div class="container-fluid">
      <seccion-servicios></seccion-servicios>
    </div>
    <news-api></news-api>
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class=" col mt-5" v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>
    <seccion-footer></seccion-footer>
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import SeccionMenu from './components/SeccionMenu.vue'
import SeccionBanner from './components/SeccionBanner.vue'
import SeccionServicios from './components/SeccionServicios.vue'
import NewsApi from './components/NewsApi.vue'
import TeamCard from './components/TeamCard.vue'
import SeccionFooter from './components/SeccionFooter.vue'


export default {
  name: 'App',
  components: {
    /* HelloWorld, */
    SeccionMenu,
    SeccionBanner,
    SeccionServicios,
    NewsApi,
    TeamCard,
    SeccionFooter
  },
  data(){
    return {
      team: [
        {
          codigo: 1,
          nombre: "Mauricio Nieto",
          descripcion: "Videojuegos, peliculas y estudiar ciencia de datos",
          rol: "Data Scientics",
          image: "https://avatars0.githubusercontent.com/u/40520725?s=400&u=6837860f6f2ef86b4cebdde47adc4f292ca9ac4f&v=4"/*  */
        },{
          codigo: 2,
          nombre: "James Pulido",
          descripcion: "Jugar futbol, estudiar ciencias de ingeneria",
          rol: "Backend Developer",
          image: "https://avatars3.githubusercontent.com/u/66868718?s=400&u=f01bb51dbf33dc57efedd54ca5519663361ba44d&v=4"
        },{
          codigo: 3,
          nombre: "Diana Galvis",
          descripcion: "Peliculas superheroes, leer libros de ciencia",
          rol: "Data Analytics",
          image: "https://avatars3.githubusercontent.com/u/75101723?s=400&v=4"
        },{
          codigo: 4,
          nombre: "Angélica Gutiérrez",
          descripcion: "Ciclismo de ruta en fines de semana y voleyball",
          rol: "FrontEnd Developer",
          image: "https://avatars2.githubusercontent.com/u/73972397?s=400&u=4b5fdfff6a4c83c85eff09b50cbf8cb284923a39&v=4"
        },{
          codigo: 5,
          nombre: "Luis Rey",
          descripcion: "practicar futbol americano y halterofilia,  y mucho Rock!",
          rol: "Database Administrator",
          image: "https://avatars1.githubusercontent.com/u/14154559?s=400&u=4057f675a7319d208aeafd6d36e33f29aea45ba5&v=4"
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: "Times New Roman", Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #093a6b;
  margin-top: 0px;
}
</style>
