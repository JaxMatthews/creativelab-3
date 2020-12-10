<template>
<div>
  <h1>Movies I Would and Would Not Watch</h1><br>
  <MovieList :movies="movies" />
</div>
</template>

<script>
import MovieList from "../components/MovieList.vue"
export default {
  name: 'Home',
  components: {
    MovieList
  },
  data() {
    return {
    }
  },
  computed: {
    movies() {
      return this.$root.$data.movies;
    }
  },
}
</script>
<style>
h1 {text-align: center;}

</style>
