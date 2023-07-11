<script setup>
import { ref } from 'vue';
const message = ref("Hello, World!")

const buttonAttrs = {
  disable: true,
  class: 'fancy-button'
}

function changeText() {
  message.value = 'Goodbye, world'
}

</script>

<template>
  <button v-bind="buttonAttrs" @click="changeText">Change to "Goodbye, world"</button>
  <span>Message: {{ message.toUpperCase() }}</span>
  <span>Message: {{ Math.random() }}</span>
</template>

<style scoped>
button {
  margin-bottom: 2em;
}

span {
  display: block;
}

.fancy-button {
  background-color: #2E85C7;
  color: white;
  border: none;
  font-weight: bold;
  padding: 0.4em 0.8em;
  border-radius: 1em;
  cursor: pointer;
}
</style>
