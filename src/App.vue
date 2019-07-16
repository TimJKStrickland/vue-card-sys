<template>
  <div id="app">
    <Cards v-bind:cards="cards"/>
  </div>
</template>

<script>
import Cards from './components/Cards.vue'

export default {
  name: 'app',
  components: {
    Cards
  },
  data() {
    return {
      cards: [
        {
          "id":"Nerium",
               "tags":["CMS Selection", "Experience Design"],
               "image":"http://herodigi....jpg",
               "title":"Nerium: Reimagining the CX for Nerium International",
               "description":"As Nerium Internation....",
               "featured":0
        },
        {
          "id":"Nerium",
               "tags":["CMS Selection", "Experience Design"],
               "image":"http://herodigi....jpg",
               "title":"Nerium: Reimagining the digital CX for Nerium International",
               "description":"As Nerium Internation....",
               "featured":0
        }
      ]
    }
  }
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
