<template>
  <div class="componente">
    <h1>Componente com renderização condicional</h1>
    <p>Tutor: {{ nome }}</p>
    <p v-if="quantidade === 0 || !quantidade">Não tem cachorros</p>
    <p v-else-if="quantidade === 1">Tem um cachorro</p>
    <p v-else>Tem mais de um cachorro</p>
  </div>
</template>

<script setup>
  defineProps({
    nome: String,
    quantidade: Number
  })
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