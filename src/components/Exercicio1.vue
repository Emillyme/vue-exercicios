<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue';

const hello = ref("Hello World!")
const mar = ref("Ondas")

function ola(){
  mar.value = "Baleia" // atirbui valor
  console.log(mar.value);
}

</script>

<template>
    <h1>Exercicio 1</h1>
    <p>Imprima uma mensagem de uma variável que mostre na tela:</p>

    <p class="content">
        {{ hello }}
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
        font-size: 18px;
        font-weight: bold;
    }
</style>
