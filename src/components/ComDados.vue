<template>
  <div>
    <h1>Componente com dados</h1>
    <p>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
  </div>
</template>

<script setup>
  let nomeProduto = "Lápis"
  let codigoProduto = "#123"
</script>

<style scoped>
  div {
    text-align: center;
    border: 2px solid #0a4504;
    background-color: #050d04;
    border-radius: 5px;
    margin: 30px;
    padding: 10px;
  }

  p {
    font-size: 1.2rem;
  }
</style>