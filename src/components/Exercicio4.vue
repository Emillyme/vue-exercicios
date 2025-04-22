<script setup lang="ts">
    import { RouterLink, RouterView } from 'vue-router'
    import { reactive, ref } from 'vue';

    const numeros = ref([1, 2, 3])

    const classObject = reactive({
        'desaparecer': false
    })

    function alterarLista(){
        classObject['desaparecer'] = !classObject['desaparecer']
    }

    function empurrarNumero(){
        numeros.value.push(numeros.value.length + 1)
        console.log(numeros.value)
    }

    function largarNumero(){
        numeros.value.pop()
    }

    function inverterLista(){
        numeros.value.reverse()
    }

</script>

<template>
    <h1>Exercicio 4</h1>
    <p>Faça 4 botões, um de alternar lista (esconder), empurrar numero (add numero a lista), largar número (deletar numero da lista) e inverter número (inverter a lista).</p>
    
    <button
        @click="alterarLista()"
    >
        Alternar Listar
    </button>
    
    <button
        @click="empurrarNumero()"
    >
        Empurrar número
    </button>
    
    <button
        @click="largarNumero()"
    >
        Largar número
    </button>
    
    <button
        @click="inverterLista()"
    >
        Inverter lista
    </button>

    
    <ul 
        :class="classObject"
    >
        <li v-for="num in numeros">
            {{ num }}
        </li>
    </ul>

    <p v-if="classObject['desaparecer']">
        A lista não foi deletada, apenas esta escondida.
    </p>
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

    button{
        margin-right: 10px;
    }

    .desaparecer{
        display: none;
    }
</style>
