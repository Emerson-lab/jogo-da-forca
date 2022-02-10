<template>
  <div class="jogo">
    <Forca :erros="erros" />
    <Palavra
      :palavra="palavra"
      :dica="dica"
      :verificarLetra="verificarLetra"
      :etapa="etapa"
    />
    <Teclado
      :letras="letras"
      :verificarLetra="verificarLetra"
      :jogar="jogar"
      v-if="etapa === 'jogo'"
    />

    <Final
      v-if="etapa !== 'jogo'"
      :etapa="etapa"
      :texto="etapa === 'enforcado' ? 'Perdeu :(' : 'Parabéns :)'"
      :jogarNovamente="jogarNovamente"
    />
  </div>
</template>

<script>
import Forca from "./Forca";
import Palavra from "./Palavra";
import Teclado from "./Teclado";
import Final from "./Final";

export default {
  name: "Jogo",
  props: {
    erros: Number,
    palavra: String,
    dica: String,
    verificarLetra: Function,
    etapa: String,
    letras: Array,
    jogar: Function,
    jogarNovamente: Function,
  },
  data() {
    return {};
  },
  components: {
    Forca,
    Palavra,
    Teclado,
    Final,
  },
  methods: {},
};
</script>

<style scoped>
.jogo {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
</style>
