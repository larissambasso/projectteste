<template>
  <section class="card">
    <img>
    <h3>Card 1</h3>
    <button>Clique aqui</button>
  </section>
</template>

<script>
  defineProps({
    card:{

    }
  })
</script>

<style scoped>
  img{
    height: 100px;
    width: auto;
  }
  .card{
    background-color: black;
  }
</style>

