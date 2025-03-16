<script setup>
defineProps({
  heading: {
    type: String,
    default: 'Legal'
  },
  description: {
    type: String,
    default: ''
  }
})
</script>

<template>
  <header class="header-section" :style="{ background: 'linear-gradient(90deg, rgba(0,0,228,1) 0%, rgba(2,114,218,1) 35%, rgba(0,85,231,1) 100%)' }">
    <div class="overlay d-flex align-items-center h-100">
      <section class="w-100">
        <div class="container text-center text-white">
          <div class="row">
            <div class="col" data-aos="fade-in">
              <h1>{{ heading }}</h1>
              <p>{{ description }}</p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </header>
</template>

