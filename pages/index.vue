<template>
  <div>
    <home-header />
    <main>
      <home-brief-steps />
      <home-features />
      <home-testimonials />
      <home-services />
      <home-faqs />
      <tools />
      <home-start-now />
    </main>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'Home',
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
})
</script>
