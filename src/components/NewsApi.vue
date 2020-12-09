<template>
    <section>
        <a name="news"></a>
        <div>
            <div class="row mt-md-5 mt-sm-5 mt-xs-5 bg-dark text-white">
                <div class="col-lg-6 col-xs-12"  v-for="(movie, index) of movies" :key="index">
                    <div class="d-flex justify-content-center align-items-center">
                        <div class="p-3">
                            <img src="https://m.media-amazon.com/images/M/MV5BMGVmMWNiMDktYjQ0Mi00MWIxLTk0N2UtN2ZlYTdkN2IzNDNlXkEyXkFqcGdeQXVyODE5NzE3OTE@._V1_SX300.jpg" alt="movie poster">
                        </div>
                        <div class="p-2">
                            <h2>{{movie.Title}}</h2>
                            <hr>
                            <h5>Sinopsis</h5>
                            <p>
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore harum natus, aut, voluptate maiores saepe delectus
                                accusamus quibusdam officiis fugiat consequatur minus fugit, fuga asperiores! Eveniet alias doloremque
                                ratione dolorum!
                            </p>
                        </div>
                    </div>
                        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                        <a :href="'https://www.imbd.com/title' + movie.imbdID" target="_blank" class="btn btn-outline-secondary ">Información</a>
                        </div>
                    <!-- //   <button type="button" class="btn btn-secondary">Secondary</button> -->
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import axios from 'axios';

export default {
    name:'NewsApi',
    data(){
        return{
            movies:null
        }
    },
    mounted(){
        axios
        .get ("http://www.omdbapi.com/?s=harry&type=movie&apikey=98a8f356")
        .then(response => {
            (this.movies = response.data.Search.slice(0,4))
                console.log(this.movies)
            })
    }
}
</script>

<style scoped>

</style>