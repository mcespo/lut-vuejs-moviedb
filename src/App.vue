<template>
  <div id="app">
    <Header />
    <MoviesList />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MoviesList from './components/MoviesList.vue'

export default {
  name: 'app',
  data() {
    return {
    };
  },
  components: {
    MoviesList,
    Header
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
