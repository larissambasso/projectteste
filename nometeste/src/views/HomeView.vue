<template>
  <main>
      <Header titulo='meu header' 
      />
    <div class="row">
      <Cards v-for="dado in dados" :key="dado.id" 
        :imagem=dado.imagem
        :botao=dado.botao
        :titulo=dado.titulo
      />
    </div>
      <Times 
      />
      <Footer
      />
    
  </main>
</template>

<script>
import Cards from '@/components/Cards.vue'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Times from '@/components/Times.vue'

export default{
  name:'HomeView',
  components:{
    Cards,
    Header,
    Footer,
    Times
  },
  data(){
    return{
      dados: []
    }
  },
  created(){
    this.dados=
      [
        {
        id:1,
        imagem:'https://static-wp-tor15-prd.torcedores.com/wp-content/uploads/2019/05/copa-sul-americana.png',
        botao: 'https://www.conmebol.com/pt-br/copa-sul-americana/',
        titulo:'COPA SULAMERICANA'
      },
      {
        id:2,
        imagem:'https://static-wp-tor15-prd.torcedores.com/wp-content/uploads/2019/05/copa-sul-americana.png',
        botao: 'https://www.conmebol.com/pt-br/copa-sul-americana/',
        titulo:'COPA SULAMERICANA'
      },
      {
        id:3,
        imagem:'https://static-wp-tor15-prd.torcedores.com/wp-content/uploads/2019/05/copa-sul-americana.png',
        botao: 'https://www.conmebol.com/pt-br/copa-sul-americana/',
        titulo:'COPA SULAMERICANA'
      },
      {
        id:4,
        imagem:'https://static-wp-tor15-prd.torcedores.com/wp-content/uploads/2019/05/copa-sul-americana.png',
        botao: 'https://www.conmebol.com/pt-br/copa-sul-americana/',
        titulo:'COPA SULAMERICANA'
      },
      {
        id:5,
        imagem:'https://static-wp-tor15-prd.torcedores.com/wp-content/uploads/2019/05/copa-sul-americana.png',
        botao: 'https://www.conmebol.com/pt-br/copa-sul-americana/',
        titulo:'COPA SULAMERICANA'
      },
      ]
  },
  beforeMount(){
  }
}

</script>

<style scoped>
  .row{
    display: flex;
    justify-content: center;
    padding: 10%;
  }

</style>
