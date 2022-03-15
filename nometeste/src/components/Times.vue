<template>
  <div class="teste">
    <h2>TIMES</h2>
        <div v-for="escudos in times" v-bind:key="escudos.id"><!-- o comando v-bind:key (é quem chama o id do objeto) -->
          <img class="times" v-bind:src="escudos.url"> <!-- este comando é o mesmo que :src="escudos.url" -->
        </div>
        <p v-on:click="maiuscula" class="campeao">
          {{mensagem}}
        </p>
  </div>
</template>
<!-- Data é uma função, que chama o return, que vai gerar um array(lista) de elementos, no caso times -->
<!-- Só podemos ter uma funçao data por componente -->
<script>
export default {
  name:'Times',
  data(){ 
    return{
      times:[
        {
          id:1,
          nome:'corinthians',
          url:'https://upload.wikimedia.org/wikipedia/pt/b/b4/Corinthians_simbolo.png'
        },
        {
          id:2,
          nome: 'palmeiras',
          url:'https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Palmeiras_logo.svg/1200px-Palmeiras_logo.svg.png'
        },
        {
          id:3,
          nome: 'sao paulo',
          url: 'https://a2.espncdn.com/combiner/i?img=%2Fi%2Fteamlogos%2Fsoccer%2F500%2F2026.png'
        },
        {
          id:4,
          nome: 'santos',
          url: 'https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Santos_logo.svg/1200px-Santos_logo.svg.png'
        }
      ]
    }
  },
}
//name: 'campeao',
//data(){
//  return{
//    mensagem:'Este time é campeao'
//  }
// },
// methods:{
//  maiuscula(){
//   this.mensagem = this.mensagem.toUpperCase();
// }
</script>

<style scoped>
  .times{
    max-height: 100px;
    width: auto;
  }
</style>