<template>
  <div class="card">
        <img :src="getUrl(Media.poster_path)" >
      <h2>{{Media.title || Media.name }}</h2>
      <h3>{{Media.original_title || Media.original_name}}</h3>
      <p >Lingua originale: <lang-flag :iso="(Media.original_language)"/></p>
      <p>Voto: {{Media.vote_average}}</p>
  </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'CardElement',
    props: {
        Media: Object,
    },
    components: {
        LangFlag,
    },
    methods: {
        getUrl(url){
            return `https://image.tmdb.org/t/p/w185/${url}`
        }
    }
}
</script>
<style lang="scss" scoped>

</style>