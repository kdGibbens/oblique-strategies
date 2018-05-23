<template>
  <div class="oblique-strategies">
    <h1>Oblique Strategies</h1>
    <h2>By Brian Eno & Peter Schmidt</h2>
    <div class="card">
      <h3 class="card-text">{{card.strategy}}</h3>
    </div>
    <div class="btn">
      <button @click.prevent="randomCard">New Card</button>
    </div>
  </div>
</template>

<script>
import obliqueStratgies from '../assets/obliqueStrategies.json'
export default {
  name: 'ObliqueStrategies',
  data () {
    return {
      cards: obliqueStratgies,
      card: ''
    }
  },
  methods: {
    randomCard () {
      this.card = this.cards[Math.floor(Math.random() * this.cards.length)]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
