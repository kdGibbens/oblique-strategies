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
      card:''
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
  body {
    margin: 0;
    padding: 0;

  }
  .card {
    width: 350px;
    height: 200px;
    background: #f8f8ff;
    box-shadow: 0 0 5px 0 rgba(50,50,50,.75);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;
    padding: 1rem;
    border-radius: 1rem;
  }
  .btn {
    margin-top: 1rem;
  }
  button {
    width: 10rem;
    height: 2rem;
    border: none;
    background: #bb3a23;
    border-radius: 1rem;
    color: #f8f8ff;
    font-size: 1rem;
    font-weight: 700;
    opacity: 0.9;
  }
  button:hover {
    opacity: 1;
  }
  button:focus {
    outline: none;
  }
</style>
