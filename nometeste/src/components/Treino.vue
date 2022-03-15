<template>
  <section class="pokemon">
    <p>{{soma(120)}}</p>
    <div v-for="(item, index) in pokemon" :key="index"><!-- quando nao tivermos id, o index serve como chave para localizar cada objeto-->
      <img :src="buscarImagem(index+1)">
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
      this.pokemon = json.results;
    });
  },
  methods:{
    buscarImagem: (index) => {
      return 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/'+index+'.png'
    },
    soma: (valorUm) => {
      return valorUm*3
    }
  }
}
</script>

<style scoped>

</style>