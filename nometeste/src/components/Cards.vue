<template>
  <section class="card">
    <img v-if="'not'!==imagem" :src='imagem'>
    <h3>{{titulo}}</h3>
    <a target="blank" v-if="'not'!==botao" :href="botao">
    <button>Jogos de hoje</button>
    </a>
  </section>
</template> 

<script>
export default {
    name: 'card',
    props: {
      imagem:{
        type: String,
        default: 'not'
      },
      botao: {
        type: String,
        default: 'not'
      },
      titulo:{
        type: String,
        required: true
      }
    }
  }

</script>

<style scoped>
  .card{
    background-color: rgb(145, 133, 133);
    border: 10px solid #ccc;
    width: 300px;
    height: 300px;
    display: flex; 
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    position: relative;
    margin-right: 15px;
  }
  h3{
    position: absolute;
    top: 5%; 
  }
  img{
    position: relative;
    height: 100px;
    width: auto;
    top: 30%;
  }
  button{
    position: relative;
    bottom: 20%;
    height: 40px;
    width: 100px;
  }

</style>

