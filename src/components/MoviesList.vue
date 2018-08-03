<template>
  <ul>
    <li v-for="movie in movies">
      <Movie :movie="movie" />
    </li>
  </ul>
</template>

<script>
  import Movie from './Movie.vue';
  export default {
    name: 'MoviesList',
    data() {
      return {
        movies: []
      }
    },
    created: function(){
      this.fetchData();
    },
    methods: {
      fetchData: async function(){
        try {
          const res = await fetch('https://api.themoviedb.org/3/discover/movie?sort_by=popularity.desc&api_key=198c27d36e884f8226446016f0cfc7e4')
          const movies = await res.json();
          this.movies = movies.results;
        }
        catch (e) {
          console.log(e);
        }
      }
    },
    components: {
      Movie
    }
  }
</script>

<style scoped>

</style>