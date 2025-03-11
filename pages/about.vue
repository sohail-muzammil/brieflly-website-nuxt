<template>
  <section>
    <p>This page will be displayed at the /about route.</p>
  </section>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'About',
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
})
</script>
