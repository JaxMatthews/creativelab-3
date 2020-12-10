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

        <h2>{{movie.score}}</h2>
        <button class="button2" v-on:click="removeMovie(movie.id, movie.name, movie.image, movie.score)">Remove From List</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'RemoveList',
  props: {
    movies: Array
  },
  methods: {
    removeMovie(id, name, score, image)
    {
      let n = this.$root.$data.aYes.indexOf(
      {
        id: id,
        name: name,
        score: score,
        image: image,
      });

      return this.$root.$data.aYes.splice(n,1);

    }
  }


}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
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
  background: #F2921D;
  color: #000;
  padding: 10px 30px;
  height: 80px;
}

.info h1 {
  font-size: 16px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
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
