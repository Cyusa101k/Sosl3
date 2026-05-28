<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/footer.vue'
</script>

<template>
  <Navbar />
  <main class="app-content">
    <RouterView />
  </main>
  <Footer />
</template>
