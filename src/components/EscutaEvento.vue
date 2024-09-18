<template>
  <div class="componente">
    <h1>Escuta evento</h1>
    <p>Total: R${{ total }}</p>
    <div class="lista">
      <EmiteEvento item="Item1" :preco="1.99" v-on:foi-adicionado="atualizarTotal"/>
      <EmiteEvento item="Item2" :preco="2.99" v-on:foi-adicionado="atualizarTotal"/>
      <EmiteEvento item="Item3" :preco="3.99" v-on:foi-adicionado="atualizarTotal"/>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import EmiteEvento from './EmiteEvento.vue';

const total = ref(0)

function atualizarTotal(preco) {
  total.value += preco 
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

  .lista {
    display: flex;
    justify-content: space-around;
  }
</style>