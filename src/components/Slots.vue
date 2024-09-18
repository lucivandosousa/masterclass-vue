<template>
  <div class="componente">
    <h1>Componente com slots</h1>
    <button class="button">
      <slot name="icone"></slot>
      <slot name="texto"></slot>
    </button>
  </div>
</template>

<script setup>

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

  .button {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: auto;
    gap: 0.5rem;
  }
</style>