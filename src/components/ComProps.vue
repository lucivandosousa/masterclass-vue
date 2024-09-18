<template>
  <div class="componente">
    <h1>Componente com props</h1>
    <p>{{ produto }} R${{ preco.toFixed(2) }}</p>
  </div>
</template>

<script setup>
  defineProps({
    produto: String,
    preco: Number
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