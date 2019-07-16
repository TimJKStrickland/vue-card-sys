<template>
  <div class="hello">
    <div v-bind:key="card.id" v-for="card in cards">
      <Card v-bind:card="card" />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  name: 'Cards',
  props: ['cards'],
  components: {
    Card
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
