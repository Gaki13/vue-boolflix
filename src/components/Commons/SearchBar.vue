<template>
    <div class="Search container">
        <form class="d-flex" @submit.prevent="searching()">
            <input type="text" class="form-control" placeholder="Search film" v-model="searchText" required>
            <button type="submit" class="btn btn-primary">Search</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
import data from '../../shared/data'

export default {
    name: 'SearchBar',
    data() {
        return{
            searchText: '',
            data,
        };
    },
    methods: {
        searching() {
            axios.get('https://api.themoviedb.org/3/search/movie', {
            params: {
                api_key: 'ee7e3a1176734bbf1587f1f1f990d694',
                query: this.searchText,
                language: 'it-IT'
            }
        }) .then((response) => {
            this.data.films = response.data.results;
            this.searchText = ''
            console.log(response);
        }).catch((error) => {
            console.log(error);
        })
        }
    },
}
</script>

<style lang="scss" scoped>

</style>