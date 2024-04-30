<script setup>
import {ref} from "vue"

let num = ref(0)
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark border-bottom border-body fixed-top">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/"><img src="https://res.cloudinary.com/dkfzj9tmk/image/upload/v1677166689/backend-project/Rick-And-Morty-Logo-Transparent-File_arpmel.png" alt=""></router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbar" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="main">
      <router-view></router-view>
  </div>

  <footer class="text-light">
    <div id="textFooter">
      Unimar | ADS | {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Caveat:wght@400..700&family=DM+Serif+Display:ital@0;1&family=IBM+Plex+Serif:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&family=Jersey+15+Charted&family=Jersey+25&family=Noto+Sans+KR:wght@100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&display=swap');

.navbar{
  background: linear-gradient(black 90%, #12b1c9ae );
}

.navbar-brand img{
  width: 280px;
  height: 70px;
}

#navbarNav{
  padding-left: 900px;
}

.nav-link{
  font-weight: bold;
  color: #12B0C9;
  font-family: "IBM Plex Serif", serif;
  font-size: 30px;
}

footer{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    background-color: black;
  }
</style>