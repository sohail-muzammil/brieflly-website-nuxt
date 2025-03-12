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
    <div class="overlay h-100 pt-5">
      <section>
        <div class="container text-center text-white mt-5 pt-5">
          <div class="row pt-5">
            <div class="col">
              <h1 class="display-3 fw-bold">{{ heading }}</h1>
              <p>{{ description }}</p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </header>
</template>

