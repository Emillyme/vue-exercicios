<script setup lang="ts">
    import { RouterLink, RouterView } from 'vue-router'
    import { reactive, ref } from 'vue';

    const numero = ref(0)

    function adicionarNumero(){
        numero.value += 1
    }

</script>

<template>
    <h1>Exercicio 5</h1>
    <p>Faça um botão de contagem</p>

    <h1>{{ numero }}</h1>
    <button @click="adicionarNumero()">
        Contar
    </button>
    <hr>
</template>

<style scoped>
    p{
        font-size: 18px;
        margin-bottom: 12px;
    }

    .content{
        color: rgb(255, 90, 90);
        font-size: 30px;
    }

    h1{
        margin-top: 30px;
        font-size: 18px;
        font-weight: bold;
    }

    a{
        display: block;
        margin-top: 10px;
    }
</style>
