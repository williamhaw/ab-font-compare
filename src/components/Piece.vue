<template>
  <textarea
    v-bind:style="{ fontFamily: font }"
    v-model="content"
    class="piece"
  />
</template>

<script>
export default {
  name: "Piece",
  props: {
    content: String,
    font: String
  }
};
</script>

<style>
.piece {
  border-style: hidden;
  resize: none;
}
</style>
