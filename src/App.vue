<script setup>

import { ref } from 'vue';

const num1 = ref(null);
const num2 = ref(null);
const result = ref(0);

function calculateP() {
  result.value = num1.value + num2.value;
}

function calculateM() {
  result.value = num1.value - num2.value;
}

function calculateT() {
  result.value = num1.value * num2.value;
}

function calculateD() {
  result.value = num1.value / num2.value;
}

</script>

<template>
  <input v-model="num1" type="number" placeholder="Enter number 1">
  <input v-model="num2" type="number" placeholder="Enter number 2">
  <div class="buttons">
    <button @click="calculateP()">+</button>
    <button @click="calculateM()">-</button>
    <button @click="calculateT()">*</button>
    <button @click="calculateD()">/</button>
  </div>
  <p>Result: {{ result }}</p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>