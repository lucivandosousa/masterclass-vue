<template>
  <div class="componente">
    <h1>Componente com renderização de lista</h1>
    <p>Tutor: {{ nome }}</p>
    <p v-if="cachorros.length === 0">Não tem cachorros</p>
    <ul v-else>
      <li v-for="cachorro in cachorros">
        🐶 Nome: {{ cachorro.nome }} 🦴 Idade: {{ cachorro.idade }}
      </li>
    </ul>
  </div>
</template>

<script setup>
  defineProps({
    nome: String,
    cachorros: Array
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

  li {
    list-style: none;
  }
</style>
