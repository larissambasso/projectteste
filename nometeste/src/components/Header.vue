<template>
  <div class="header">
    <nav class="menu">
      <ul>
        <li><a v-if="'not'!==titulo" :href="titulo">Pagina principal</a></li>
        <li><a v-if="'not'!==titulo" :href="titulo">Campeonatos</a></li>
        <li><a v-if="'not'!==titulo" :href="titulo">Jogos</a></li>
      </ul>
    </nav>
  </div>
</template>

<script setup>
  defineProps({
    menu:{
      type:String,
    },
    titulo:{
      type:String,
      default:'not'
    },
  })
</script>

<style scoped>
  .menu{
    position: relative;
    width: 100%;
  }
  ul{
    width: 100%;
    height: 70px;
    background: gray;
    top: 0%;
    padding-left: 3%;
    padding-right: 10%;
    display: flex;
    justify-content: space-around;
    align-items: center;

  }
  li{
    list-style-type:none;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgb(40, 181, 216);
    width: 170px;
    height: 40px;
    border-radius: 7px;
  }
  a{
    text-decoration: none;
    font-size: 18px;
    color: white;
  }
</style>