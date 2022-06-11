<template>
  <section>
      <div class="container-fluid">
                <div class="row ">
                    <h1>Films trovati:</h1>
                    <div v-for="film in data.films" :key="film.id" class="col-3 my-5"><CardElement :Media="film" /></div>
                </div>
                <div class="row">
                    <h1>Serie TV trovate:</h1>
                    <div v-for="serie in data.series" :key="serie.id" class="col-3 my-5"><CardElement :Media="serie"/></div>    
                </div>
                
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