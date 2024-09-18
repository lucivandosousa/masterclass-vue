<template>
  <div class="componente">
    <h1>Componente com propriedades assistidas</h1>
      <p>{{ idade }}</p>
      <div class="itens">
        <label for="">Ano Nascimento: 
          <input type="number" v-model="anoNascimento" min="1900">
        </label>
        <label for="">Ano Atual: 
          <input type="number" v-model="anoAtual" min="2000">
        </label>
      </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

const anoNascimento = ref(1900)
const anoAtual = ref(2000)
const idade = ref(0)

watch(anoAtual, (anoAlterado) => {
  idade.value = anoAlterado - anoNascimento.value
})

watch(anoNascimento, (anoAlterado) => {
  idade.value = anoAtual.value - anoAlterado
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

  .itens {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem
  }
</style>