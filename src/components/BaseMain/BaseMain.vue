<template>
    <main>
        <MainSection/>
    </main>
</template>

<script>
import MainSection from '../Commons/MainSection.vue'

export default {
    name: 'BaseMain',
    components: {
        MainSection,
    },
}
</script>

<style lang="scss" scoped>
    main{
        min-height: calc(100vh - 128px);
    }
</style>