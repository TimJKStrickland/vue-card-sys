<template>
  <div class="card">
    <div>
      <img v-bind:src="this.carta.image" class="card-image" alt="" />
    </div>
    <p class="title">{{ this.carta.title }}</p>
    <div class="back">
      <p v-bind:key="tag" v-for="tag in this.carta.tags">
      {{ tag }}
      </p>
    </div>
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
.card-image {
  width: 100%;
}
  .back {
    display: none;
  }
  .card {
    flex-direction: column;
  }
</style>
