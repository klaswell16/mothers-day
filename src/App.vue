<script setup>
import { ref } from 'vue';
const transition = ref(false);
</script>

<template>
  
  <div v-if="transition === false" class="image-container">
    <img
      class="card-image main-image"
      alt="boys waiting"
      src="/boys_waiting.png"
    />
    <button 
      class="overlay-button" 
      @click="transition = true"
    >
    
    </button>
    <img
      class="card-image hover-image"
      alt="boys waiting - hover state"
      src="/boys_pressin.png"  
    />
    
  </div>
  <div v-if="transition">
    <img 
      class="card-image"
      alt=" "
      src="/boys_lovin.png" 
      >
  </div>
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

.main-image {
  position: relative;
  z-index: 1;
  transition: opacity 0.3s ease;
}

.hover-image {
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  z-index: 2;  
  transition: opacity 0.3s ease;
}

.overlay-button {
  position: absolute;
  bottom: 55%;
  right: 45%;
  background: transparent;
  border: 2px solid black;
  color: white;
  padding: 60px 90px;
  cursor: pointer;
  border-radius: 5px;
  z-index: 3;  
  
}


.overlay-button:hover ~ .hover-image {
  opacity: 1;
}


.overlay-button:hover ~ .main-image {
  opacity: 0;
}
</style>