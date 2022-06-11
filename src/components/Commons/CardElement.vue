<template>
  <div class="card">
        <img :src="getUrl(Media.poster_path)" >
        <h2>{{Media.title || Media.name }}</h2>
        <h3>{{Media.original_title || Media.original_name}}</h3>
        <p >Lingua originale: <lang-flag :iso="(Media.original_language)"/></p>
        <h6>Voto: <span v-html="voteStar(Media.vote_average)"></span><font-awesome-icon icon="fa-solid fa-star" /></h6>
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
        },
        voteStar(vote){
            let StarsHtml = ' ';
            for (let i = 0; i < Math.ceil(vote / 2); i++) {
                StarsHtml += '<font-awesome-icon icon="fa-solid fa-star"/>';
            }
            return StarsHtml;
        }

    }
}
</script>
<style lang="scss" scoped>
    .star{
        color: red;
    }
</style>