<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import colourLogic from "../composables/colourLogic.js"

export default {
  setup() {
    const { colors, message, matchColor } = colourLogic();

    console.log(colors, message, );

    return { colors, message, matchColor };
  },
};
</script>

<style></style>
