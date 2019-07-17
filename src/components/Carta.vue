<template>
  <div class="card">
    <h1>{{ this.carta.title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Carta',
  props: ['carta'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .card{
    flex-basis: 33%;
    max-width: 33%;
    display: flex;
  }
</style>
