<template>
  <div class="forca">
    <!--<img :src="`../img/${erros}.svg`" />-->
    <img
      :src="`https://raw.githubusercontent.com/dimascapelari/jogoForcaVueJS/b862d9dd25121065eb4a4a3f2e5abcc814c74784/src/assets/${erros}.svg`"
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