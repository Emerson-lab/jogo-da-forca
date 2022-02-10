<template>
  <div class="teclado">
    <button
      class="teclado-botao"
      v-for="(letra, key) in 'abcdefghijklmnopqrstuvwxyz'"
      :key="key"
      :disabled="verificarLetra(letra)"
      v-on:click="jogar(letra)"
    >
      {{ letra }}
    </button>
  </div>
</template>

<script>
export default {
  name: "Teclado",
  props: {
    letras: Array,
    verificarLetra: Function,
    jogar: Function
  },
  data() {
    return {};
  },
  components: {},
  methods: {},
};
</script>

<style scoped>
.teclado {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 85%;
  margin-top: 20px;
}

.teclado button {
  margin: 5px;
  text-transform: uppercase;
  width: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
