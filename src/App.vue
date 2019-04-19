<template>
  <div id="app">
    <Piece content="Welcome to Your Vue.js App" :font="font" />
  </div>
</template>

<script>
import Piece from "./components/Piece.vue";
var WebFont = require("webfontloader");

export default {
  name: "app",
  components: {
    Piece
  },
  data() {
    return {
      font: "Oswald"
    };
  },
  methods: {
    downloadFont(font) {
      WebFont.load({
        google: {
          families: [font]
        }
      });
    }
  },
  mounted() {
    this.downloadFont(this.font);
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
