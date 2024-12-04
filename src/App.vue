<script setup>
//inserir a lógica
//ref é uma função que cria dados reativos
//para acessar os dados do ref é preciso utilizar a palavra .value
import {ref} from "vue";
const numero = ref(0);

//lógica dos botões
//função aumentar
function aumentar() {
  numero.value ++
}

//função diminuir
function diminuir() {
  if(numero.value > 0) {
    numero.value --
  }
}
</script>

<template>
<!-- inserir tags e componentes -->
<h1>Contador</h1>
<h2>{{ numero }}</h2>
<!-- para pegar o evento do clique, usaremos o v-on:click ou o atalho @ -->
<button @click="aumentar">+</button>
<button @click="diminuir">-</button>
</template>

<style>
/* inserir o estilo do site */

</style>