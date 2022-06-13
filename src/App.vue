<template>
  <div id="app">
   <MainHeader/>
   <BaseMain/>
  </div>
</template>

<script>
import MainHeader from './components/BaseHeader/MainHeader.vue'
import BaseMain from './components/BaseMain/BaseMain.vue'

export default {
  name: 'App',
  components: {
    MainHeader,
    BaseMain,
  }
}
</script>

<style lang="scss">
  @import url(./assets/global.scss);
  #app{
    background-color: black;
  }
</style>
