<template>
  <div class="convite">
    <img src="/images/convite.png" alt="Convite" class="convite-image" />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
/* Centralizar o convite na tela */
.convite {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 50%; /* Centraliza verticalmente */
  left: 50%; /* Centraliza horizontalmente */
  transform: translate(-50%, -50%); /* Ajusta a centralização precisa */
}

/* Diminuir o tamanho da imagem do convite */
.convite-image {
  width: 400px; /* Reduzido para 400px, você pode modificar conforme necessário */
  height: auto; /* Mantém a proporção da imagem */
}
</style>
