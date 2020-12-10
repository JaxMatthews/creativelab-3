<template>

<div class="wrapper">

  <div class="movies">
    <div class="movie" v-for="movie in movies" :key="movie.id">
      <div class="info">
        <h1>{{movie.name}}</h1>
      </div>
      <div class="image">
        <img :src="'/images/'+movie.image">
      </div>
      <div class="score">
        <button class="button1" v-on:click="addWould(movie.id, movie.name, movie.image, movie.score)">Would Watch</button>
        <h2>{{movie.score}}</h2>
        <button class="button2" v-on:click="addWouldNot(movie.id, movie.name, movie.image, movie.score)">Would NOT Watch</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'MovieList',
  props: {
    movies: Array
  },
  methods: {
    addWouldNot(id, name, image, score)
    {
    return this.$root.$data.aNo.push({
      id: id,
      name: name,
      score: score,
      image: image

    })  },
    addWould(id, name, image, score)
    {
    return this.$root.$data.aYes.push({
      id: id,
      name: name,
      score: score,
      image: image

    })  },

  }

}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  background: lightblue;
}

.movies {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.movie {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.movie img {
  border: 2px solid #333;
  height: 250px;
  width: 200px;
  object-fit: cover;
}

.movie .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background: black;
  color: white;
  padding: 10px 15px;
  height: 60px;
}

.info h1 {
  font-size: 15px;
}

.info h2 {
  font-size: 14px;
}

.score {
  display: flex;
}

.button1 {
  height: auto;
  background: green;
  color: white;
  border: none;
}
.button2 {
  height: auto;
  background: red;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>
