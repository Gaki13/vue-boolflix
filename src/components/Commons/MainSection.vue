<template>
  <section>
      <ul>
          <li v-for="film in Films" :key="film.id"><CardElement :Film="film" /></li>
      </ul>    
  </section>
</template>

<script>
import axios from 'axios'
import CardElement from './CardElement.vue'
import data from '../../shared/data'

export default {
    name: 'MainSection',
    components: {
        CardElement,
    },
    data() {
        return{
            films: [],
            data,
        };
    },
    created() {
        axios.get('https://api.themoviedb.org/3/movie', {
            params: {
                api_key: 'ee7e3a1176734bbf1587f1f1f990d694',
                query: 'ritorno',
                language: 'it-IT'
            }
        }) .then((response) => {
            this.films = response.data.results;
            console.log(response);
        }).catch((error) => {
            console.log(error);
        });
    },
    computed() {
        return this.Films
    },
}
</script>

<style lang="scss" scoped>

</style>