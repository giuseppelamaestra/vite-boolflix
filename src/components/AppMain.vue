<template>
   <SearchBar @searched="getMovies"/>
   <MoviesList :movies="MoviesList"/>
</template>
<script>

import axios from 'axios';



import SearchBar from './SearchBar.vue';
import MoviesList from './MoviesList.vue';
export default {
    name : 'AppMain',

    data(){
        return {
            moviesApiUrl : 'https://api.themoviedb.org/3/search/movie',
            MoviesList : [],
        }
    },

    components : {
         SearchBar,
         MoviesList,
    },
    methods : {
   

         getMovies(searcheInput){
            axios.get(this.moviesApiUrl, {
                params : {  
                  api_key: 'ccfd4451a0b08c098e69339b74b1f549',
                  query : searcheInput,
                       }
                     } )
              .then( (response) => {
               // handle success
                 console.log(response.data.results);
                 this.MoviesList = response.data.results;
                                 })
              .catch(function (error) {
                // handle error
               console.log(error);
                   })
                .finally(function () {
                   // always executed
                   });
         },
     
    },
    created(){

    },
}
</script>
<style lang="scss">

</style>