<template>
    <v-container>
      <v-row>
        <v-col
          v-for="movie in movies"
          :key="movie.id"
          cols="12"
          sm="6"
          md="4"
        >
          <MovieCard
            :image="movie.image"
            :title="movie.title"
            :rating="movie.rating"
            :duration="movie.duration"
          />
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  import MovieCard from '~/components/MovieCard.vue'
  
  export default {
    components: {
      MovieCard
    },
    data() {
      return {
        movies: [
          {
            id: 1,
            image: 'path/to/image1.jpg',
            title: 'Movie Title 1',
            rating: 4.5,
            duration: '1h30m'
          },
          {
            id: 2,
            image: 'path/to/image2.jpg',
            title: 'Movie Title 2',
            rating: 4.0,
            duration: '1h45m'
          },
          // Ajoutez d'autres films ici
        ]
      }
    }
  }
  </script>
  