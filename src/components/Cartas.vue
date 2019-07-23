<template>
  <div class="hello">
    <div class="card" v-bind:key="carta.id" v-for="carta in cartas">
      <Carta v-bind:carta="carta" />
    </div>
  </div>
</template>

<script>
import Carta from './Carta.vue';
// import axios from 'axios';
export default {
  name: 'Cartas',
  props: ['cartas'],
  components: {
    Carta
  },
  // methods: {
    // getData(){
      // let config = {
      //   headers: {
      //     'Accept': 'headers/json'
      //   }
      // };
      // axios.get('https://s3-us-west-1.amazonaws.com/hero-engineering-public/interview/fe-code-challenge.json', config)
      //   .then(res => { this.cartas = res.data.cards; })
      //   .catch(err => this.cartas = err)
    // }
  // },
  // data(){
    // return { cartas: getData() }
  // },
  // created: function(){
  //  this.getData();
  // },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello {
    padding: 1rem;
    display: flex;
    box-sizing: border-box;
    flex-wrap: wrap;
  }

  .card {
    flex-basis: 33%;
    max-width: 33%;
    display: flex;
  }
</style>
