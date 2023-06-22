<template>
  <div>
    <input type="text" name="movie-search" id="movie-search" v-model=" searchInput">
    <button @click="$emit('searched', searchInput)"> Search</button>
  </div>
</template>
<script>
export default{
    name : 'SearchBar',
    props: {

    },

    data() {
        return {
            searchInput : ''
        }

    },

    methods : {
        log(message) {
            console.warn(message);
         }
    },
}
</script>
<style lang="scss">
</style>