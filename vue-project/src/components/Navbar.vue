<script setup>
import {RouterLink, RouterView} from 'vue-router'
</script>

<template>
   <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <RouterLink class="navbar-brand" to="/">Rehab</RouterLink>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="/">Home<span class="sr-only"></span></a></li>
      <li class="nav-item">
        <RouterLink a class="nav-link" to="/about">About</RouterLink>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Pricing</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Disabled</a>
      </li>
    </ul>
  </div>
</nav>
<RouterView/>
</template>
