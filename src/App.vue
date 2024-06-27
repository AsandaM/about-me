<template>
  <!-- Logo -->
  <div class="text-center">
        <!-- <a href="./index.html"><img src="https://asandam.github.io/images/Asanda_Mehlo-logo2.png" alt="Logo" class="logo"></a> -->
    </div>
  <nav class="navbar navbar-expand-lg navbar-light sticky-top">
    <div class="container-fluid">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-center" id="navbarNav">   
              <!-- <ul class="navbar-nav">
                    <li class="nav-item"><router-link to="/"> Home</router-link></li>
                    <li class="nav-item"><router-link to="/about"> About</router-link></li>
                </ul> -->
                <header>
    <div class="menu">
      <router-link to="/">
        <span class="outter">
          <span class="inner">HOME</span>
        </span>
      </router-link>
      <router-link to="/about">
        <span class="outter">
          <span class="inner">PHOTOGRAPHY</span>
        </span>
      </router-link>
    </div>
  </header>
            </div>
        </div>
  </nav>
  
  
  <router-view/>
</template>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  
}

/* nav {
  padding: 30px;
} */
body{
  background: linear-gradient(to right, #F5F5F5 0%, #F5F5F5 50%, #C9CC3F 50%, #C9CC3F 100%);
}

nav a.router-link-exact-active {
  border-bottom: 2px solid #aa7b4c; /* Highlight the active link */
}
nav a:hover {
  color:  #007bff;
}

.navbar {
    /* padding: 1rem 2rem; */
    background-color: #F5F5F5;
    /* background-color: transparent; */
    

}

header {
  height: 3rem;
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #0f0e0d;
  padding: 1.5rem 1rem;
}

.menu {
  display: flex;
}

.menu a {
  text-decoration: none;
  margin: 0 1rem;
  color: #100f0f;
  position: relative;
  display: block;
  z-index: 999;
  font-size: 20px;
}

.outter::before,
.outter::after,
.inner::before,
.inner::after {
  content: "";
  position: absolute;
  background: #080808;
  transition: transform 0.6s ease;
}

.outter::before,
.outter::after {
  height: 1px;
  width: calc(100% + 12px);
  top: 0;
  left: -8px;
  transform: scale(0);
}

.outter::after {
  bottom: 0;
  transform-origin: right;
}

.inner::before,
.inner::after {
  width: 1px;
  height: calc(100% + 10px);
  top: -5px;
  transform: scale(0);
}

.inner::before {
  left: -2px;
  transform-origin: bottom;
}

.inner::after {
  right: 0;
  transform-origin: top;
}

.menu a:hover .outter::before,
.menu a:hover .outter::after,
.menu a:hover .inner::before,
.menu a:hover .inner::after {
  transform: scale(1);
}
</style>
