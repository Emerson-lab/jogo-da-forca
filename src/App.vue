<template>
  <div id="app">
    <h1>Jogo da Forca</h1>
    <section id="inicio" v-if="tela === 'inicio'">
      <Formulario />
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
    };
  },
  components: {
    Formulario,
  },
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
