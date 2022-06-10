<template>
  <div class="card">
      <h2>{{Film.title}}</h2>
      <h3>{{Film.original_title}}</h3>
      <p >Lingua originale: <lang-flag :iso=" SelectFlag(Film.original_language)"/></p>
      <p>Voto: {{Film.vote_average}}</p>
  </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'CardElement',
    props: {
        Film: Object,
    },
    components: {
        LangFlag,

    },
    methods:{  
        SelectFlag(language){
            return language == "vi" ? "it , es , en , fr, de" : language ;
        }
    },
}
</script>
<style lang="scss" scoped>

</style>