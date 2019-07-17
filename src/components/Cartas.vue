<template>
  <div class="hello">
    <div v-bind:key="carta.id" v-for="carta in cartas">
      <Cartas v-bind:card="card" />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  name: 'Cartas',
  props: ['cartas'],
  components: {
    Carta
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
