<template>
  <div class="card">
        <img :src="getUrl(Media.poster_path)" >
        <div class="overlay">
            <h2>{{Media.title || Media.name }}</h2>
            <h3>{{Media.original_title || Media.original_name}}</h3>
            <p >Lingua originale: <lang-flag :iso="(Media.original_language)"/></p>
            <h6>Voto: <font-awesome-icon icon="fa-solid fa-star"  class="star" v-for=" vote in voteStar(Media.vote_average)"  :key="vote"/></h6>  
            <p>Overview: {{Media.overview}}</p>
        </div>     
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
            if(url == null){
                return `https://via.placeholder.com/398x598.png`
            }
            return `https://image.tmdb.org/t/p/w185/${url}`
        },
        voteStar(vote){
            return Math.ceil(vote / 2) ;
        }

    }
}
</script>
<style lang="scss" scoped>
    .star{
        color: yellow;
    }
    .card{
        position: relative;
    }

    .card:hover .overlay{
        opacity: 1;
    }
    
    .overlay{
        opacity: 0;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        color:white;
        background-color: black;
        overflow: auto;
    }
</style>