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
              <ul class="navbar-nav">
                    <li class="nav-item"><router-link to="/"> Home</router-link></li>
                    <li class="nav-item"><router-link to="/about"> About</router-link></li>
                </ul>
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
template{
  background: linear-gradient(to right, #F5F5F5 0%, #F5F5F5 50%, #C9CC3F 50%, #C9CC3F 100%);
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
}

nav a.router-link-exact-active {
  border-bottom: 2px solid #aa7b4c; /* Highlight the active link */
}
nav a:hover {
  color:  #007bff;
}

.navbar {
    /* padding: 1rem 2rem; */
    background-color: #FFF8F3;
    /* background-color: transparent; */
    

}
</style>
