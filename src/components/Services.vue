<template>
  <section id="services" class="bg-white py-20">
    <div class="mx-auto max-w-screen-2xl px-2 sm:px-4 lg:px-6">
      <div class="max-w-2xl">
        <p class="flex items-center gap-3 text-xl font-semibold uppercase tracking-[0.28em] text-emerald-600/80">
          <span class="h-px w-10 bg-emerald-400/70" />
          Services
        </p>
        <h2 class="mt-4 text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl leading-tight">
          Un accompagnement complet, du design à la mise en production
        </h2>
        <p class="mt-4 text-lg leading-relaxed text-gray-600">
          Nous construisons des expériences web propres et des solutions data et d'intelligence artificielle exploitables, avec une attention particulière à la performance et à la clarté.
        </p>
      </div>

      <div class="mt-12 grid gap-6 md:grid-cols-2 lg:grid-cols-4">
        <div class="group relative rounded-3xl bg-white p-6 text-center shadow-[0_12px_40px_-28px_rgba(0,0,0,0.35)] ring-1 ring-gray-100 transition hover:-translate-y-1 hover:shadow-[0_18px_50px_-30px_rgba(0,0,0,0.45)]">
          <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-2xl bg-gray-900 text-white shadow-sm transition group-hover:scale-105">
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M4.5 5.25A.75.75 0 015.25 4.5h13.5a.75.75 0 01.75.75v9.75a.75.75 0 01-.75.75H5.25a.75.75 0 01-.75-.75V5.25z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M9.75 19.5h4.5" />
            </svg>
          </div>
          <h3 class="mt-5 text-lg font-semibold text-gray-950">Sites Web</h3>
          <p class="mt-2 text-sm leading-relaxed text-gray-600">
            Sites vitrines et landing pages orientés design, SEO et performance.
          </p>
        </div>

        <div class="group relative rounded-3xl bg-white p-6 text-center shadow-[0_12px_40px_-28px_rgba(0,0,0,0.35)] ring-1 ring-gray-100 transition hover:-translate-y-1 hover:shadow-[0_18px_50px_-30px_rgba(0,0,0,0.45)]">
          <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-2xl bg-emerald-600 text-white shadow-sm transition group-hover:scale-105">
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M3.75 5.25A1.5 1.5 0 015.25 3.75h3.5a1.5 1.5 0 011.5 1.5v3.5a1.5 1.5 0 01-1.5 1.5h-3.5a1.5 1.5 0 01-1.5-1.5v-3.5z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M3.75 15.25a1.5 1.5 0 011.5-1.5h3.5a1.5 1.5 0 011.5 1.5v3.5a1.5 1.5 0 01-1.5 1.5h-3.5a1.5 1.5 0 01-1.5-1.5v-3.5z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M13.75 5.25a1.5 1.5 0 011.5-1.5h3.5a1.5 1.5 0 011.5 1.5v3.5a1.5 1.5 0 01-1.5 1.5h-3.5a1.5 1.5 0 01-1.5-1.5v-3.5z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M13.75 15.25a1.5 1.5 0 011.5-1.5h3.5a1.5 1.5 0 011.5 1.5v3.5a1.5 1.5 0 01-1.5 1.5h-3.5a1.5 1.5 0 01-1.5-1.5v-3.5z" />
            </svg>
          </div>
          <h3 class="mt-5 text-lg font-semibold text-gray-950">Applications Web</h3>
          <p class="mt-2 text-sm leading-relaxed text-gray-600">
            Dashboards, outils internes, CRM, SaaS : produits stables et scalables.
          </p>
        </div>

        <div class="group relative rounded-3xl bg-white p-6 text-center shadow-[0_12px_40px_-28px_rgba(0,0,0,0.35)] ring-1 ring-gray-100 transition hover:-translate-y-1 hover:shadow-[0_18px_50px_-30px_rgba(0,0,0,0.45)]">
          <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-2xl bg-sky-600 text-white shadow-sm transition group-hover:scale-105">
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <rect x="7" y="7" width="10" height="10" rx="2" stroke-width="1.75" />
              <rect x="10" y="10" width="4" height="4" rx="1" stroke-width="1.75" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M9 3v3m6-3v3m-6 12v3m6-3v3M3 9h3M3 15h3m12-6h3m-3 6h3" />
            </svg>
          </div>
          <h3 class="mt-5 text-lg font-semibold text-gray-950">Intelligence Artificielle</h3>
          <p class="mt-2 text-sm leading-relaxed text-gray-600">
            POC, prétraitement des données, intégration, automatisation : une intelligence artificielle utile, mesurable et maintenable.
          </p>
        </div>

        <div class="group relative rounded-3xl bg-white p-6 text-center shadow-[0_12px_40px_-28px_rgba(0,0,0,0.35)] ring-1 ring-gray-100 transition hover:-translate-y-1 hover:shadow-[0_18px_50px_-30px_rgba(0,0,0,0.45)]">
          <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-2xl bg-gray-100 text-gray-900 shadow-sm transition group-hover:scale-105">
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M4.5 4.5v15a.75.75 0 00.75.75h13.5" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M8.25 17.25v-6m4.5 6V7.5m4.5 9.75V12" />
            </svg>
          </div>
          <h3 class="mt-5 text-lg font-semibold text-gray-950">Analyse de données</h3>
          <p class="mt-2 text-sm leading-relaxed text-gray-600">
            Nettoyage, dashboards, KPI et recommandations pour décider plus vite.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>
