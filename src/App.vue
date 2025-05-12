<script setup>
import { ref } from 'vue';
const transition = ref(false);
</script>

<template>
  <header>working</header>
  <div class="image-container">
    <img
      class="card-image"
      alt="boys waiting"
      src="/boys_waiting.png"
    />
    <button 
      class="overlay-button" 
      @click="transition = true"
    >
      click me
    </button>
  </div>
  <div v-if="transition">trans</div>
</template>

<style scoped>
.image-container {
  position: relative; 
  display: inline-block; 
}

.card-image {
  height: 800px;
  width: 1200px;
  display: block;
}

.overlay-button {
  position: absolute;
  bottom: 55%; 
  right: 50%;  
  
  
  background: transparent;
  border: 2px solid black;
  color: white;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
  border-radius: 5px;
}

.overlay-button:hover {
  background: rgba(255, 255, 255, 0.2);
}
</style>