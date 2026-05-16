<script setup lang="ts">
import Navbar from './components/navbar/Navbar.vue'
import Hero from './components/hero/Hero.vue'
import Features from './components/features/Features.vue'
import Staff from './components/staff/Staff.vue'
import CTA from './components/cta/CTA.vue'
import Footer from './components/footer/Footer.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col font-sans selection:bg-primary/30">
    <Navbar />
    <main class="flex-grow">
      <Hero />
      <Features />
      <Staff />
      <CTA />
    </main>
    <Footer />
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
}
</style>
