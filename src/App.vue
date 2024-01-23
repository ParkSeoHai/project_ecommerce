<template>
  <Header />
  <main>
    <div class="container p-0">
      <RouterView />
    </div>
  </main>
  <Footer />
</template>

<script setup>
import Header from '@/components/Header.vue';
import Footer from './components/Footer.vue';
</script>