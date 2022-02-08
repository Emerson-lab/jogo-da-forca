<template>
  <div id="app">
    <h1>Jogo da Forca</h1>
    <section id="inicio" v-if="tela === 'inicio'">
      <Formulario
        v-if="etapa === 'palavra'"
        title="Defina a palavra"
        button="Próximo"
        :action="setPalavra"
      />
      <Formulario
        v-if="etapa === 'dica'"
        title="Defina a dica"
        button="Iniciar o game :)"
      />
    </section>
    <section id="jogo" v-if="tela === 'jogo'">Jogo</section>
  </div>
</template>

<script>
import "./css/global.css";

import Formulario from "./components/Formulario";

export default {
  name: "App",
  data() {
    return {
      tela: "inicio",
      etapa: "palavra",
    };
  },
  components: {
    Formulario,
  },
  methods: {
    setPalavra: function(palavra) {
      alert(palavra)
    }
  }
};
</script>

<style>
#app {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
