<script setup>
import MeuComponente from "./components/MeuComponente.vue";
import ComDados from "./components/ComDados.vue";
import DadosReativos from "@/components/DadosReativos.vue"
import OneDataBinding from "./components/OneDataBinding.vue";
import TwoDataBinding from "./components/TwoDataBinding.vue";
import ComProps from "./components/ComProps.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
import PropriedadesComputadas from "./components/PropriedadesComputadas.vue";
import PropriedadesAssistidas from "./components/PropriedadesAssistidas.vue";
import PropriedadesAssistidasEffect from "./components/PropriedadesAssistidasEffect.vue";
import RenderizacaoCondicional from "./components/RenderizacaoCondicional.vue";
import RenderizacaoDeListas from "./components/RenderizacaoDeListas.vue";
import Slots from "./components/Slots.vue";

const cachorros = [
  {
    nome: "Salame",
    idade: 1
  },
  {
    nome: "Cheide",
    idade: 2
  },
  {
    nome: "Pugas",
    idade: 3
  }
]
</script>

<template>
  <header>Vue.js 3</header>
  <Slots>
    <template v-slot:icone>
      <svg xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-home"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 12l-2 0l9 -9l9 9l-2 0" /><path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" /><path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" /></svg>
    </template>
    <template v-slot:texto>
      <span>Home</span>
    </template>
  </Slots>
  <RenderizacaoDeListas nome="Sousa" :cachorros="cachorros"/>
  <RenderizacaoCondicional nome="Sousa" :quantidade="0"/>
  <PropriedadesAssistidasEffect />
  <PropriedadesAssistidas />
  <PropriedadesComputadas />
  <EscutaEvento />
  <ComProps produto="Produto" v-bind:preco="30.50"/>
  <TwoDataBinding />
  <OneDataBinding />
  <DadosReativos />
  <ComDados />
  <MeuComponente />
</template>

<style scoped>

</style>
