<template>
  <section class="pokemon">
    <div v-for="item of pokemon" :key="item.id">
      <h2>MEUS POKEMONS</h2>
      <img :src='item.url'>
      <p>{{item.name}}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'pokemon',
  data(){
    return{
      pokemon:[]
    }
  },
  created(){
    fetch('https://pokeapi.co/api/v2/pokemon')
    .then(mostrar => mostrar.json())
    .then(json => {
      this.pokemon = json;
    });
  }
}
</script>

<style scoped>

</style>