<template>
  <div class="card">
      <h2>{{Film.title}}</h2>
      <h3>{{Film.original_title}}</h3>
      <p>{{Film.original_language}}</p>
      <p>{{Film.vote_average}}</p>
  </div>
</template>

<script>
export default {
    name: 'CardElement',
    props: {
        Film: Object,
    }
}
</script>

<style lang="scss" scoped>

</style>