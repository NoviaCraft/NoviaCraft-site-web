<template>
  <header class="fixed inset-x-0 top-0 z-50 border-b border-gray-200/70 bg-white/75 backdrop-blur">
    <nav class="mx-auto flex max-w-screen-2xl items-center justify-between px-2 py-4 sm:px-4 lg:px-6">
      <a href="#" class="group inline-flex items-baseline gap-2">
        <span class="text-lg font-semibold tracking-tight text-gray-900">NovIACraft</span>
        <span class="text-xs font-medium text-gray-500 group-hover:text-gray-700 transition-colors">Web • IA</span>
      </a>

      <div class="hidden md:flex items-center gap-7">
        <a href="#services" class="text-sm font-medium text-gray-700 hover:text-gray-900 transition-colors">Services</a>
        <a href="#produits" class="text-sm font-medium text-gray-700 hover:text-gray-900 transition-colors">Produit</a>
        <a href="#realisations" class="text-sm font-medium text-gray-700 hover:text-gray-900 transition-colors">Réalisations</a>
        <a href="#apropos" class="text-sm font-medium text-gray-700 hover:text-gray-900 transition-colors">Équipe</a>
        <a
          href="#contact"
          class="inline-flex items-center rounded-full bg-emerald-600 px-5 py-2 text-sm font-semibold text-white shadow-sm hover:bg-emerald-500 transition-colors"
        >
          Parler de votre projet
        </a>
      </div>

      <button
        type="button"
        @click="toggleMenu"
        class="md:hidden inline-flex items-center justify-center rounded-lg p-2 text-gray-700 hover:bg-gray-100 transition"
        aria-label="Ouvrir le menu"
      >
        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </nav>

    <div v-if="mobileMenuOpen" class="md:hidden border-t border-gray-200/70 bg-white/85 backdrop-blur">
      <div class="mx-auto max-w-screen-2xl px-2 py-4 space-y-2 sm:px-4 lg:px-6">
        <a href="#services" class="block rounded-lg px-3 py-2 text-sm font-medium text-gray-800 hover:bg-gray-100">Services</a>
        <a href="#produits" class="block rounded-lg px-3 py-2 text-sm font-medium text-gray-800 hover:bg-gray-100">Produit</a>
        <a href="#realisations" class="block rounded-lg px-3 py-2 text-sm font-medium text-gray-800 hover:bg-gray-100">Réalisations</a>
        <a href="#apropos" class="block rounded-lg px-3 py-2 text-sm font-medium text-gray-800 hover:bg-gray-100">Équipe</a>
        <a href="#contact" class="block rounded-lg px-3 py-2 text-sm font-semibold text-white bg-emerald-600 hover:bg-emerald-500">
          Parler de votre projet
        </a>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const mobileMenuOpen = ref(false);

const toggleMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};
</script>
