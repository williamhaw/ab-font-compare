<template>
  <div id="app">
    <Piece content="Welcome to Your Vue.js App" font="Oswald" />
  </div>
</template>

<script>
import Piece from "./components/Piece.vue";

var WebFont = require("webfontloader");

WebFont.load({
  google: {
    families: ["Oswald"]
  }
});

export default {
  name: "app",
  components: {
    Piece
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
