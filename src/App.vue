<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <section class="container">


    <h1 class="top">Welcome to the AI Playground</h1>
    <div class="vid-holder container">
      <video autoplay muted loop class="vidd">
        <source src="src/assets/LakeSmall.mp4" type="video/mp4">
      </video>
    </div>

    <RouterView />

  </section>
</template>

<style scoped>
.container {
  position: relative;
  width: 100%;
  height: 100vh;
  max-height: 820px;
  
  display: grid;
  place-items: center;

}
.top {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding: 0.25rem;
  text-align: center;
  color: white;
  font-size: 2rem;
  font-weight: 900;
  text-shadow: 0 0 10px black;
  background-color: rgba(0,0,0,0.5);
}
.vid-holder {
  position: absolute;
  z-index: -1;
  width: 100%;
  height: 100vh;
}

.vidd {
  width: 100%; 
  height: 100%; 
  max-width: 960px;
  max-height: 600px;
  object-fit: fill;
}
</style>
