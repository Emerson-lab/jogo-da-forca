<template>
  <div class="forca">
    <img
      :src="`https://raw.githubusercontent.com/william-costa/wdev-hangman-game-resources/master/images/hangman/${erros}.svg`"
      alt="Imagem de uma forca"
      title="Forca"
    />
  </div>
</template>

<script>
export default {
  name: "Forca",
  props: {
    erros: Number,
  },
  data() {
    return {};
  },
  components: {},
  methods: {},
};
</script>

<style scoped>
.forca img {
  height: 100px;
}
</style>
