<template>
    <header>
        <div class="row align-items-center">
            <div class="col-6"><img src="../../assets/img/netflix-logo.png" alt=""></div>
            <div class="col-5 space-between"> <SearchBar/> </div>
        </div>
        
    </header>
</template>

<script>
import SearchBar from '../Commons/SearchBar.vue'

export default {
    name: 'MainHeader',
    components: {
        SearchBar,
    },
}
</script>

<style lang="scss" scoped>
    header{
        height: 128px;
        .row{
            height: 100%;
            .col-6{
                height: 100%;
                img{
                    height: 100%;
                }
            }
        }
    }
</style>