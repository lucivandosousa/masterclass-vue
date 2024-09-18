<template>
  <div class="componente">
    <h1>Componente com dados reativos</h1>
    <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
    <button v-on:click="fazerAniversario">Fazer aniversário</button>
    <button v-on:click="mudarNome">Mudar Nome</button>
    <hr>
    <h1>Componente com dados reativos</h1>
    <p>Nome: {{ pet.nome }} | Idade: {{ pet.idade }}</p>
    <button v-on:click="fazerAniversarioPet">Fazer aniversário</button>
    <button v-on:click="mudarNomePet">Mudar Nome</button>
  </div>
</template>

<script setup>
  import { reactive, ref } from 'vue';

  const nome = ref("Sousa")
  const idade = ref(20)

  const pet = reactive({
    nome: "Simba",
    idade: 1
  })

  function fazerAniversario() {
    idade.value++
  }

  function mudarNome() {
    nome.value = "Outro nome"
  }

  function fazerAniversarioPet() {
    pet.idade++
  }

  function mudarNomePet() {
    pet.nome = "Outro nome"
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

  hr {
    margin-top: 20px;
    border: 2px solid #13b939;
  }
</style>