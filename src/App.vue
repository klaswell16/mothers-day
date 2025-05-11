<script setup>
import { ref } from 'vue';
const transition = ref(false)

</script>

<template>
  <header>
    working
  </header>
  <div>
    <button @click="transition = true">click me</button>
  </div>
  <div v-if="transition === true">
    trans
  </div>
</template>

<style scoped>

</style>
