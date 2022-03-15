<template>
  <div class="equipes">
    <h2>Equipes brasileiras</h2>
    <div v-for="item of equipes" :key="item.id" > <!--A cada posiçao da lista equipes(variavel declarada no array, o resultado vai exibir nome,escudo e pontos-->
      <p>{{item.nome}}</p>
      <img :src='item.escudo'>
      {{item.pontos}}
    </div>
  </div>
</template>

<script>
export default {
  name:'equipes',
  data(){
    return{
      equipes:[]
    }
  },
  created() {//ciclo de vida de um componente
    fetch('https://hackthon-decola.firebaseio.com/clubes-lista.json?print=pretty')
    .then(resultado => resultado.json()) 
    .then(json => {
      this.equipes = json;
    });
  }
}
</script>

<style scoped>

</style>