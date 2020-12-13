<template>
    <div>
        <a name="news"></a>
        <div class="row mt-md-5 mt-sm-5 mt-xs-5 bg-dark text-white">
            <div class="col-lg-6 col-xs-12"  v-for="(movie, index) of movies" :key="index">
                <div class="d-flex justify-content-center align-items-center">
                    <div class="p-3">
                        <img :src="movie.Poster">
                    </div>
                    <div class="p-2">
                        <h2>{{movie.Title}}</h2>
                    <br>
                        <h3>{{movie.imdbID}}</h3>
                        <p>IMDB</p>
                        <h3>{{movie.Year}}</h3>
                        <p>Estreno</p>             
                        
                        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                            <a :href="'https://www.imbd.com/title/' + movie.imbdID" class="btn btn-outline-secondary ">Información</a>
                        </div>
                    </div>
                </div>
            </div>
        <!-- //   <button type="button" class="btn btn-secondary">Secondary</button> -->
        </div>
    </div>
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
        axios.get ("http://www.omdbapi.com/?s=Claude&type=movie&apikey=98a8f356")
        /* fetch("http://www.omdbapi.com/?s=harry&type=movie&apikey=98a8f356") */
        .then(response => {
            this.movies = response.data.Search.slice(0,4)
                console.log(this.movies)
            })
        
    }
}
</script>

<style scoped>

</style>