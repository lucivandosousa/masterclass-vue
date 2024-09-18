<template>
  <div class="componente">
    <h1>Emite evento</h1>
    <p>{{ produto }} R${{ preco.toFixed(2) }}</p>
    <button v-on:click="adicionar">Adicionar ao carrinho</button>
  </div>
</template>

<script setup>
  const props = defineProps({
    produto: String,
    preco: Number
  })

  const emit = defineEmits(["foiAdicionado"])

  function adicionar() {
    emit("foiAdicionado", props.preco)
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