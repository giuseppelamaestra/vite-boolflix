<template>
  <div>
    <article v-for="movie in movies">

        <h2>
            {{ movie.title }}
        </h2>

        <h4>
             {{ movie.original_title }}
        </h4>

          <img v-if="isLanguageFlagPresent(movie.original_language)" :src="getImagePath(movie.original_language)" alt="">
          <span v-else>
            {{ movie.original_language }}
          </span>
    </article>
  </div>
</template>
<script>
export default {
    name: 'MoviesList',
    props: {
       movies : Array
    },
    methods : {
            isLanguageFlagPresent(language){
            if (this.availableFlags.includes(language+'.png')){
              return true 
            }
              return false 
            },

            getImagePath(img){
              return new URL(`../assets/img/flags/${img}.png`, import.meta.url).href;
            }
    },
    data(){
           return{
            availableFlags : [ 'en.png', 'it.png', 'fr.png ']
           }
    },
}
</script>
<style lang="scss">
</style>