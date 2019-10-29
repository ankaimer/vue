<template>
  <div>
      <h1>Film List</h1>
      <b-card-group columns :key="film.id" v-for="film in films">
        <FilmCard :film="film"/>
      </b-card-group>
      
  </div>
</template>

<script>

import FilmCard from './FilmCard.vue'

export default {
    components: {
        FilmCard
    },

    data: function() {
            return { 
                films: [
                    {id: 1, name: 'Rocky', rating: 3, image: require('../assets/rocky.jpeg')},
                    {id: 2, name: 'DeadPool', rating: 5, image: require('../assets/deadpool.jpeg')},
                    {id: 3, name: 'La La Land', rating: 0, image: require('../assets/lalaland.jpeg')}
                ]            
            }
    }
    
}

</script>

<style>

</style>