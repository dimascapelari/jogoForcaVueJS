<template>
  <div class="jogo">
    <CompForca :erros="erros" />

    <CompPalavra
      :palavra="palavra"
      :dica="dica"
      :verificarLetra="verificarLetra"
      :etapa="etapa"
    />

    <CompTeclado
      v-if="etapa === 'jogo'"
      :letras="letras"
      :verificarLetra="verificarLetra"
      :jogar="jogar"
    />

    <CompFinal
      v-if="etapa != 'jogo'"
      :etapa="etapa"
      :texto="etapa === 'ganhador' ? 'Parabéns :)' : 'Tadinho :('"
      :jogarNovamente="jogarNovamente"
    />
  </div>
</template>

<script>
import CompForca from "./CompForca.vue";
import CompPalavra from "./CompPalavra.vue";
import CompTeclado from "./CompTeclado.vue";
import CompFinal from "./CompFinal.vue";

export default {
  name: "CompJogo",
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
  methods: {},
  components: {
    CompForca,
    CompPalavra,
    CompTeclado,
    CompFinal,
  },
};
</script>

<style>
.jogo {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
</style>