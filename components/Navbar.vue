<template>
  <nav class="navbar navbar-expand-lg navbar-light fixed-top">
    <div :class="{'container border border-1 border-light-subtle': true, 'rounded-pill': !isNavbarOpen, 'rounded-5': isNavbarOpen}" id="navbarContainer">
      <NuxtLink class="navbar-brand" to="/">
        <img src="~/assets/img/logo/logo.png" height="35" class="w-auto" alt="" />
      </NuxtLink>
      <button class="navbar-toggler" type="button" @click="isNavbarOpen = !isNavbarOpen" aria-controls="navbarSupportedContent"
        aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" :class="{ 'd-block': isNavbarOpen }" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item mx-2">
            <NuxtLink class="nav-link" to="/">Home</NuxtLink>
          </li>
          <li class="nav-item mx-2">
            <NuxtLink class="nav-link" to="/about">About</NuxtLink>
          </li>
          <li class="nav-item mx-2">
            <NuxtLink class="nav-link" to="/agency">For Agencies</NuxtLink>
          </li>
        </ul>
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0 align-items-center">
          <li class="nav-item">
            <NuxtLink class="btn btn-primary rounded-pill" to="/wishlist">Login</NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
  import { ref } from 'vue';
  const isNavbarOpen = ref(false);
</script>
