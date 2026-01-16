<template>
  <div class="app">
    <Header />
    <main>
      <Hero />
      <Services />
      <Produits />
      <Realisations />
      <About />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Services from './components/Services.vue'
import Produits from './components/Produits.vue'
import Realisations from './components/Realisations.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
.app {
  min-height: 100vh;
}
</style>

