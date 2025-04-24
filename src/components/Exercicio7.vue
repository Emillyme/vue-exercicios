<script setup lang="ts">
    // import { RouterLink, RouterView } from 'vue-router'
    import { ref, watch } from 'vue';

    const text = ref('Edit me!')
    const verificacao = ref(false)
    const nomes = ref([`Aboba`, `Abobinha`, `Abobabao`])
    const selecionados = ref([])

</script>

<template>
    <h1>Exercicio 7</h1>

    <h1>Entrada de texto</h1>
    <input v-model="text" type="text">
    <label for="">{{ text }}</label>

    <h1>Caixa de verficação</h1>
    <input v-model="verificacao" type="checkbox">
    <label for="">{{ verificacao }}</label>
    
    <h1>Múltipla caixa de verificação</h1>
    <div v-for="nome in nomes" :key="nome">
        <input type="checkbox" :value="nome" v-model="selecionados">
        <span>{{ nome }}</span>
    </div>

    <p>Nomes verificados</p>
    {{ selecionados }}

    <h1>Radio</h1>
    <input type="radio" value="1" >
    <input type="radio" value="2" >
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
