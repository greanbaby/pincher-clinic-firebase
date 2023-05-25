<script>
export default {
  name: "vidHolder",
  computed: {
    videoElement() {
      return this.$refs.video;
    }
  }
}

</script>

<template>
  <section class="container">


    <h2 class="top">Welcome to the AI Playground</h2>
    <div class="vid-holder container">
      <video autoplay muted loop class="vidd" ref="video">
        <source src="@/assets/LakeSmall.mp4" type="video/mp4">
      </video>
    </div>

    <p class="ai">
      <a class="ai-link" 
        href="https://pinchercreekgm.netlify.app/"
        target="_blank">
      Pincher Creek Greasemonkey Site
      </a>
    </p>
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
  font-size: 1.25rem;
  font-weight: 700;
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

.ai {
  position: absolute;
  top: 16%;
  color: white;
  font-weight: bold;
}
.ai-link {
  color: yellow; 
  text-decoration: none;
}</style>
