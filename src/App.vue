<template>
  <div id="app">
    <Piece :content="content" :font="fonts[0]" />
    <Piece :content="content" :font="fonts[1]" />
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
      fonts: ["Oswald", "Raleway"],
      content: "Welcome to Your Vue.js App"
    };
  },
  methods: {
    downloadFont(fonts) {
      WebFont.load({
        google: {
          families: fonts
        }
      });
    }
  },
  mounted() {
    this.downloadFont(this.fonts);
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
