<template>
  <div class="card">
      <h2>{{Film.title}}</h2>
      <h3>{{Film.original_title}}</h3>
      <p >Lingua originale: <lang-flag :iso="(Film.original_language)"/></p>
      <p>Voto: {{Film.vote_average}}</p>
  </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'CardElement',
    data(){
        return{
            
        }
    },
    props: {
        Film: Object,
    },
    components: {
        LangFlag,
    },
    methods:{  
        
    },
}
</script>
<style lang="scss" scoped>

</style>