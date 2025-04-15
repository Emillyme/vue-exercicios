<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { reactive, ref } from 'vue';

const isGreen = ref(false)
const isBlue = ref(false)

const classObject = reactive({
    'text-red': false
})
const classObject2 = reactive({
    'text-green': true,
    'text-blue': false
})


function trocar1(){
    classObject['text-red'] = !classObject['text-red']
}

function trocar2(){
    classObject2['text-blue'] = !classObject2['text-blue']
 }

</script>

<template>
    <h1>Exercicio 3</h1>
    <p>Faça uma modificação de mensagem com lógica</p>

    <div 
        class="texto"
        :class="classObject"
        @click="trocar1"
    >
        Isto deveria ser vemelho. Clica-me
    </div>

    <div
        class="texto"
        :class="classObject2"
        @click="trocar2"
        >
        Isto deveria ser verde, e deve alternar entre ver e azul sobre o clique.
    </div>
    <hr>
</template>

<style scoped>
    .texto{
        cursor: pointer;
        font-size: 16px;
    }

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

    .text-green{
        color: rgb(98, 168, 57);
    }

    .text-blue{
        color: rgb(77, 127, 192);
    }

    .text-red{
        color: red;
    }

</style>
