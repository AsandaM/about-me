<template>
  <div id="main" class="container-fluid main-section">
    <div id="main-text" class="col-md-12 main-text">
      <div class="ring-container">
        <div class="ring">
          <i style="--clr:#00ff0a;"></i>
          <i style="--clr:#ff0057;"></i>
          <i style="--clr:#fffd44;"></i>
          <div class="login">
            <img src="https://asandam.github.io/images/Me.png" alt="Your Name" class="img-fluid rounded-circle mb-4" style="max-width: 350px;">
          </div>
        </div>
        <div class="helloworld-container">
          <HelloWorld msg="Welcome to My Portfolio" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap");

body, html {
  height: 100%;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #111;
}

.container-fluid {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

#main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  /* height: 100vh; */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 50px 0;
}

#main-text {
  text-align: center;
  background-color: rgba(225, 213, 205, 0.6);
  padding: 20px;
  width: 80%;
  /* height: calc(90vh - 70px); */
}

.helloworld-container {
  background-color: inherit;
  padding: 20px;
}

.ring-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.ring {
  position: relative;
  width: 500px;
  height: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.ring i {
  position: absolute;
  inset: 0;
  border: 2px solid #C9CC3F;
  transition: 0.5s;
}

.ring i:nth-child(1) {
  border-radius: 38% 62% 63% 37% / 41% 44% 56% 59%;
  animation: animate 6s linear infinite;
}

.ring i:nth-child(2) {
  border-radius: 41% 44% 56% 59%/38% 62% 63% 37%;
  animation: animate 4s linear infinite;
}

.ring i:nth-child(3) {
  border-radius: 41% 44% 56% 59%/38% 62% 63% 37%;
  animation: animate2 10s linear infinite;
}

.ring:hover i {
  border: 6px solid var(--clr);
  filter: drop-shadow(0 0 20px var(--clr));
}

@keyframes animate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

@keyframes animate2 {
  0% {
    transform: rotate(360deg);
  }
  100% {
    transform: rotate(0deg);
  }
}

.login {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}

.login img {
  max-width: 100%;
  max-height: 100%;
  border-radius: 50%;
}

#main-text h1 {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 50px;
  font-weight: bold;
  margin-bottom: 20px;
}

#main-text p {
  font-family: 'Playfair Display', sans-serif;
  color: #555;
  line-height: 1.6;
  font-size: 1.2rem;
  margin-bottom: 20px;
}

#main-text a {
  background-color: #aa7b4c;
  color: #ffffff;
  padding: 10px 20px;
  border-radius: 5px;
  text-decoration: none;
}
</style>
