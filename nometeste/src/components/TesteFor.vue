<template>
  <div class="teste">
    <h2>TESTE FOR</h2>
      <ul>
        <li v-for="escudos in times" v-bind:key="escudos.id">
          <img v-bind:src="escudos.url">
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name:'TesteFor',
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
  }
}
</script>

<style scoped>

</style>