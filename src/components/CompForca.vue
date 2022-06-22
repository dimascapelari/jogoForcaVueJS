<template>
  <div class="forca">
    <!--<img :src="`../img/${erros}.svg`" />-->
    <img
      :src="`https://raw.githubusercontent.com/dimascapelari/jogoForcaVueJS/main/src/assets/${erros}.svg`"
    />
  </div>
</template>

<script>
export default {
  name: "CompForca",
  props: {
    erros: Number,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
.forca img {
  height: 150px;
}
</style>