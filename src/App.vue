<template>
  <div id="app" class="app">
    <!-- Envelope -->
    <Envelope v-if="showEnvelope" @opened="handleEnvelopeOpened" />

    <!-- Convite -->
    <Convite v-if="showConvite" />
  </div>
</template>

<script>
import Envelope from "./components/components/Envelope.vue";
import Convite from "./components/components/Convite.vue";

export default {
  components: {
    Envelope,
    Convite,
  },
  data() {
    return {
      showEnvelope: true,
      showConvite: false,
    };
  },
  methods: {
    handleEnvelopeOpened() {
      this.showEnvelope = false;
      this.showConvite = true;
    },
  },
};
</script>

<style>
/* Aplica uma imagem de fundo no body */
body {
  text-align: center;
  background-color: rgb(61, 15, 15);
  /*background-image: url("../public/images/");  Caminho da sua imagem de fundo */
  background-size: cover; /* Faz a imagem cobrir toda a tela */
  background-position: center; /* Centraliza a imagem de fundo */
  background-repeat: no-repeat; /* Impede a repetição da imagem */
  width: 100%;
  height: 100vh; /* Certifica-se de que o body ocupa toda a altura da tela */
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
