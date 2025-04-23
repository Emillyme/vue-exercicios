<script setup lang="ts">
    // import { RouterLink, RouterView } from 'vue-router'
    import { ref, watch } from 'vue';

    const celsius = ref('')
    const fahrenheit = ref('')

    watch(celsius, (novoValor) => {
        const numero = parseFloat(novoValor)
        if (!isNaN(numero)) {
            fahrenheit.value = ((numero * 9) / 5 + 32).toFixed(2)
        } else {
            fahrenheit.value = ''
        } 
    })

</script>

<template>
    <h1>Exercicio 6</h1>
    <p>Conversor de celsius para fahrenheit</p>

    <label for="">Celsius</label>
    <input type="text" v-model="celsius" name="" id="">
    <br>
    <label for="">Fahrenheit</label>
    <input type="text" :value="fahrenheit" disabled>
    <br>
    <br>
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

    input{
        height: 35px;
        width: 250px;
        margin-bottom: 20px;
        margin-left: 10px;
        font-size: 20px;
    }
</style>
