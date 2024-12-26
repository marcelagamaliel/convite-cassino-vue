<template>
  <div class="envelope" @click="openEnvelope">
    <img
      src="/images/envelope.png"
      alt="Envelope"
      class="envelope-image"
      :class="{ opened: isOpened }"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpened: false,
    };
  },
  methods: {
    openEnvelope() {
      this.isOpened = true;
      // Após a animação, emite o evento para o App.vue mostrar o convite
      setTimeout(() => {
        this.$emit("opened");
      }, 1000); // Tempo para a animação de rotação
    },
  },
};
</script>

<style>
/* Centralizar o envelope na tela */
.envelope {
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 50%; /* Centraliza verticalmente */
  left: 50%; /* Centraliza horizontalmente */
  transform: translate(-50%, -50%); /* Ajusta a centralização precisa */
}

/* Aumentar o tamanho da imagem do envelope */
.envelope-image {
  width: 500px; /* Tamanho aumentado */
  height: auto; /* Mantém a proporção da imagem */
  transition: transform 1s ease-in-out;
}

.envelope-image.opened {
  transform: rotateY(180deg); /* Rotação para simular a abertura */
}
</style>
