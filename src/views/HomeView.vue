<template>
   <section class="hero-section">
    <div class="hero-content animate__fadeInUp">
      <div class="img-tape">
        <div class="tape left-tape"></div>
        <div class="tape top-tape"></div>
        <div class="tape right-tape"></div>
        <div class="tape bottom-tape"></div>
        <img src="https://asandam.github.io/images/Me.png" alt="Your Name" class="img-fluid rounded-circle mb-4" style="max-width: 200px;">
      </div>
      <HelloWorld msg="Welcome to My Portfolio"/>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
  .hero-section {

      /* background-image: linear-gradient(to right, #ff7e5f, #feb47b); */
      background: linear-gradient(to right, #F5F5F5 0%, #F5F5F5 50%, #C9CC3F 50%, #C9CC3F 100%);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #fff;
      position: relative;
      overflow: hidden;
    }
    
    /* Image tape animation */
    .img-tape {
      position: relative;
      display: inline-block;
      overflow: hidden; /* Ensure tape animations stay within container */
      
    }
    .tape {
      position: absolute;
      background-color: rgba(255, 255, 255, 0.5); /* Semi-transparent for realism */
      box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2); /* Slight shadow for depth */
      border-radius: 2px; /* Slightly rounded edges */
      animation-duration: 5s; /* Duration of tape animation */
      animation-timing-function: ease-in-out; /* Smooth animation */
      animation-iteration-count: 5; /* Play animation 5 times */
    }
    .left-tape {
      top: -10px;
      left: -10px;
      width: 5px;
      height: calc(100% + 20px); /* Adjust height to cover entire image */
      transform: skewY(-15deg) rotate(5deg);
      animation-name: moveLeft;
    }
    .top-tape {
      top: -10px;
      left: -10px;
      width: calc(100% + 20px); /* Adjust width to cover entire image */
      height: 5px;
      transform: skewX(-15deg) rotate(5deg);
      animation-name: moveTop;
    }
    .right-tape {
      top: -10px;
      right: -10px;
      width: 5px;
      height: calc(100% + 20px); /* Adjust height to cover entire image */
      transform: skewY(15deg) rotate(-5deg);
      animation-name: moveRight;
    }
    .bottom-tape {
      bottom: -10px;
      left: -10px;
      width: calc(100% + 20px); /* Adjust width to cover entire image */
      height: 5px;
      transform: skewX(15deg) rotate(-5deg);
      animation-name: moveBottom;
    }
    .img-tape img {
      position: relative;
      z-index: 1;
      animation-duration: 5s;
      animation-timing-function: ease-in-out;
      animation-iteration-count: 5; /* Play animation 5 times */
      animation-name: imageDisappear;
    }
    @keyframes moveLeft {
      0%, 100% { left: -10px; }
      50% { left: calc(100% + 10px); }
    }
    @keyframes moveTop {
      0%, 100% { top: -10px; }
      50% { top: calc(100% + 10px); }
    }
    @keyframes moveRight {
      0%, 100% { right: -10px; }
      50% { right: calc(100% + 10px); }
    }
    @keyframes moveBottom {
      0%, 100% { bottom: -10px; }
      50% { bottom: calc(100% + 10px); }
    }
    @keyframes imageDisappear {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }
    
</style>
