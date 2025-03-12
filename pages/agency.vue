<template>
    <div>
        <agency-header />
        <main>
            <agency-why />
            <agency-what />
            <agency-join />
            <agency-matching />
            <tools />
            <agency-faqs />
            <agency-start-now />
        </main>
    </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'Agency',
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
})
</script>
