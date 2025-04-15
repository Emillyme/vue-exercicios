<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue';

const hello = ref("Hello World")
const exemplo = ref("")

function adicionarExclamacao(){ 
    hello.value = (hello.value += '!')
}

function inverterPalavra(){
    let charsDaFrase = hello.value.trim().split('')
    charsDaFrase.reverse();
    hello.value = charsDaFrase.join('');
}

function pararLink(e:any){
    e.preventDefault();
    alert('Evento prevenido')
}

</script>

<template>
    <h1>Exercicio 2</h1>
    <p>Faça uma mensagem ser invertida e ter adição de algum caractere específico.</p>

    <p class="content">
        {{ hello }}
    </p>

    <button @click="adicionarExclamacao">Append "!"</button>
    <button @click="inverterPalavra">inverter Palavra</button>
    <a @click="pararLink" href="https://www.youtube.com/watch?v=jI2K1xT0C6w">Uma ligação com "e.preventDefault"</a>
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
