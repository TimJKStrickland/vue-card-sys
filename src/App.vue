<template>
  <div id="app">
    <Cards v-bind:cards="cards"/>
    <Cartas v-bind:cartas="cartas" />
  </div>
</template>

<script>
import Cards from './components/Cards.vue'
import axios from 'axios';
export default {
  name: 'app',
  components: {
    Cards
  },
  methods: {
    getCards(){
      this.cartas = "CHECK THIS OUT"
      var vm = this;
      let config = {
        headers: {
          'Accept': 'headers/json'
        }
      };
      axios.get('https://s3-us-west-1.amazonaws.com/hero-engineering-public/interview/fe-code-challenge.json', config)
        .then(res => { vm.cartas = res.data.cards })
        .catch(err => vm.cartas = err)
    }
  },
  created: function(){
   this.getCards();
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
