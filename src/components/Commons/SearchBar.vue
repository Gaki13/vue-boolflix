<template>
    <div class="Search container">
        <form class="d-flex">
            <input type="text" class="form-control" placeholder="Search film" v-model="data.searchText">
            <button type="submit" class="btn btn-primary">Search</button>
        </form>
    </div>
</template>

<script>
import data from '../../shared/data'

export default {
    name: 'SearchBar',
    data() {
        return{
            data
        };
    },
}
</script>

<style lang="scss" scoped>

</style>