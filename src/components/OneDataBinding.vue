<template>
  <div class="componente">
    <h1>Componente com one way data binding</h1>
    <input type="text" v-bind:value="valor">
    <br>
    <button v-on:click="mudarInput">Mudar</button>
  </div>
</template>

<script setup>
  import { ref } from 'vue';

  const valor = ref("Vue é muito legal")

  function mudarInput() {
    valor.value = "Vue é D++"
  }
</script>

<style scoped>
  .componente {
    text-align: center;
    border: 2px solid #0a4504;
    background-color: #050d04;
    border-radius: 5px;
    margin: 30px;
    padding: 10px;
  }

  .componente p {
    font-size: 1.2rem;
  }
</style>