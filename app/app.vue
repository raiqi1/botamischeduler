<!-- app/app.vue - Ubah jadi layout simple -->
<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
// head
useHead({
  title: 'WhatsApp Scheduler',
  meta: [
    { name: 'description', content: 'Aplikasi penjadwalan pesan WhatsApp' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
    { charset: 'utf-8' }
  ],
  link: [
    { rel: 'icon', type: 'image/png', href: '/favicon.png' },
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap' }
  ]
})
</script>