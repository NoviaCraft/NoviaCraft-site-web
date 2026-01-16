<template>
  <section id="produits" class="bg-gray-50 py-20">
    <div class="mx-auto max-w-screen-2xl px-2 sm:px-4 lg:px-6">
      <div class="grid items-start gap-10 lg:grid-cols-12">
        <div class="lg:col-span-6">
          <p class="flex items-center gap-3 text-xl font-semibold uppercase tracking-[0.28em] text-emerald-600/80">
            <span class="h-px w-10 bg-emerald-400/70" />
            Produit
          </p>
          <h2 class="mt-4 text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl leading-tight">
            CRM NovIACraft
          </h2>
          <p class="mt-4 text-lg leading-relaxed text-gray-600">
            Un CRM personalisable, simple d'utilisation, rapide, à coût unique et flexible : pipeline clair, suivi des opportunités et reporting.
            Conçu pour les équipes qui veulent une vue nette et des actions concrètes.
          </p>

          <div class="mt-8 grid gap-3 sm:grid-cols-2">
            <div class="flex items-start gap-3 rounded-2xl bg-white p-4 shadow-sm">
              <div class="mt-1 rounded-full bg-green-50 p-1 text-green-700">
                <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
              </div>
              <div>
                <p class="text-sm font-semibold text-gray-950">Contacts & comptes</p>
                <p class="mt-1 text-sm text-gray-600">Centralisez l'info utile, sans friction.</p>
              </div>
            </div>

            <div class="flex items-start gap-3 rounded-2xl bg-white p-4 shadow-sm">
              <div class="mt-1 rounded-full bg-green-50 p-1 text-green-700">
                <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
              </div>
              <div>
                <p class="text-sm font-semibold text-gray-950">Pipeline & opportunités</p>
                <p class="mt-1 text-sm text-gray-600">Suivi visuel et priorisation rapide.</p>
              </div>
            </div>

            <div class="flex items-start gap-3 rounded-2xl bg-white p-4 shadow-sm">
              <div class="mt-1 rounded-full bg-green-50 p-1 text-green-700">
                <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
              </div>
              <div>
                <p class="text-sm font-semibold text-gray-950">Reporting</p>
                <p class="mt-1 text-sm text-gray-600">KPIs utiles, pas des tableaux vides.</p>
              </div>
            </div>

            <div class="flex items-start gap-3 rounded-2xl bg-white p-4 shadow-sm">
              <div class="mt-1 rounded-full bg-green-50 p-1 text-green-700">
                <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
              </div>
              <div>
                <p class="text-sm font-semibold text-gray-950">Expérience fluide</p>
                <p class="mt-1 text-sm text-gray-600">Interface simple, focus productivité.</p>
              </div>
            </div>
          </div>

          <div class="mt-8 flex flex-col gap-3 sm:flex-row">
            <a
              href="https://mike-dreeman-crm-landing.vercel.app/"
              target="_blank"
              rel="noopener noreferrer"
              class="inline-flex items-center justify-center rounded-full bg-emerald-600 px-7 py-3 text-sm font-semibold text-white shadow-sm hover:bg-emerald-500 transition"
            >
              Voir la landing CRM
              <svg class="ml-2 h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </a>
            <a href="#contact" class="inline-flex items-center justify-center rounded-full border border-gray-300 bg-white px-7 py-3 text-sm font-semibold text-gray-900 hover:bg-gray-50 transition">
              Demander une démo
            </a>
          </div>
        </div>

        <div class="lg:col-span-6">
          <div class="rounded-3xl bg-white p-6 shadow-sm">
            <div class="flex items-start justify-between gap-4">
              <div>
                <p class="text-sm font-semibold text-gray-950">Aperçu (live)</p>
                <p class="mt-1 text-sm text-gray-600">Landing CRM intégrée directement.</p>
              </div>
              <a
                href="https://mike-dreeman-crm-landing.vercel.app/"
                target="_blank"
                rel="noopener noreferrer"
                class="inline-flex items-center gap-2 rounded-full bg-gray-900 px-4 py-2 text-xs font-semibold text-white hover:bg-gray-800 transition"
              >
                Ouvrir
                <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                </svg>
              </a>
            </div>

            <div class="mt-6 overflow-hidden rounded-2xl bg-white shadow-sm">
              <div class="aspect-16/10">
                <iframe
                  title="Aperçu CRM"
                  src="https://mike-dreeman-crm-landing.vercel.app/"
                  class="h-full w-full"
                  loading="lazy"
                  referrerpolicy="no-referrer"
                />
              </div>
            </div>

            <p class="mt-3 text-xs text-gray-500">
              Si l'aperçu ne s'affiche pas, c'est souvent lié aux protections d'embed (X-Frame-Options). Dans ce cas, utilisez le bouton “Ouvrir”.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>
