<template>
  <div>
    <article v-for="movie in movies">

        <h2>
            {{ movie.title }}
        </h2>

        <h4>
             {{ movie.original_title }}
        </h4>

          <p> 
               {{ movie.original_language  }}
          </p>
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

    },
}
</script>
<style lang="scss">
</style>