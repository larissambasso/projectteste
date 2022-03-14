<template>
    <div>
        <p :class="'ddd'===texto ? 'exemplo' : 'vermelho'">{{texto}}</p>
        <img v-if="'larissa'!==endereco" :src='endereco'>
    </div>
</template>

<script setup>
    defineProps({
        texto:{
            type:String,
            default: 'ddd'
        },
        endereco:{
            type:String,
            default: 'larissa'
        }
    })
</script>
<style scoped>
    .exemplo{
        color: green;
    }
    .vermelho{
        color: red;
    }
    img{
        height: 100px;
        width: auto;
    }
</style>
