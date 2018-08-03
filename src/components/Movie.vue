<template>
  <div>
    <img :src="movie.posterPath" :alt="movie.title">
    {{movie.title}}
  </div>
</template>

<script>
  export default {
    props: ['movie']
  }
</script>

<style scoped>

</style>