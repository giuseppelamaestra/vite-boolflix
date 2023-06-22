<template>
   <SearchBar/>
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

    },
    created(){

    },
}
</script>
<style lang="scss">

</style>