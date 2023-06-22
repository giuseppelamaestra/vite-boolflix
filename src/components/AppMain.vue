<template>
   <SearchBar @searched="log"/>
   <MoviesList/>
</template>
<script>

import SearchBar from './SearchBar.vue';
import MoviesList from './MoviesList.vue';
export default {
    name : 'AppMain',
    components : {
         SearchBar,
         MoviesList,
    },
    methods : {
        log(message) {
            console.warn(message);
         }
    
    },
    created(){

    },
}
</script>
<style lang="scss">

</style>