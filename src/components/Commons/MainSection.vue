<template>
  <section>
      <div class="container">
            <ul>
                <h1>Films trovati:</h1>
                <li v-for="film in data.films" :key="film.id"><CardElement :Media="film"/></li>
                <h1>Serie TV trovate:</h1>
                <li v-for="serie in data.series" :key="serie.id"><CardElement :Media="serie"/></li>
            </ul>   
      </div>
        
  </section>
</template>

<script>
import CardElement from './CardElement.vue'
import data from '../../shared/data'

export default {
    name: 'MainSection',
    components: {
        CardElement,
    },
    data() {
        return{
            data,
        };
    },
}
</script>

<style lang="scss" scoped>

</style>