<template>
  <section id="apropos" class="relative bg-white py-24 border-t border-gray-100">
    <div class="mx-auto max-w-screen-2xl px-2 sm:px-4 lg:px-6">
      <div class="grid gap-10 lg:grid-cols-12">
        <div class="lg:col-span-5">
          <p class="flex items-center gap-3 text-xl font-semibold uppercase tracking-[0.28em] text-emerald-600/80">
            <span class="h-px w-10 bg-emerald-400/70" />
            Équipe
          </p>
          <h2 class="mt-4 text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl leading-tight">
            Deux profils complémentaires
          </h2>
          <p class="mt-4 text-lg leading-relaxed text-gray-600">
            Raphaëlle apporte la rigueur data/IA et la créativité. Mickael construit des produits web fiables et rapides.
            Ensemble, on livre des solutions propres, maintenables et orientées résultats.
          </p>

        </div>

        <div class="lg:col-span-7">
          <div class="grid gap-6 md:grid-cols-2">
            <div class="group rounded-3xl bg-white/85 p-6 shadow-sm ring-1 ring-gray-200/70 backdrop-blur transition hover:-translate-y-1 hover:shadow-md">
              <div class="flex items-center justify-between">
                <div>
                  <p class="text-base font-semibold text-gray-950">Raphaëlle HUYNH</p>
                  <p class="mt-1 text-sm text-gray-600">Co-fondatrice · Data / IA · Creative dev</p>
                </div>
                <div class="rounded-2xl bg-emerald-50 p-3 text-emerald-700 shadow-sm">
                  <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M4.5 4.5v15a.75.75 0 00.75.75h13.5" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M6.75 14.25l3-3 2.25 2.25 4.5-5.25" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M16.5 8.25h2.25v2.25" />
                  </svg>
                </div>
              </div>
              <ul class="mt-5 space-y-2 text-sm text-gray-700">
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />Analyse de données & dashboards</li>
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />IA utile (POC → prod)</li>
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />Expériences créatives</li>
              </ul>
            </div>

            <div class="group rounded-3xl bg-white/85 p-6 shadow-sm ring-1 ring-gray-200/70 backdrop-blur transition hover:-translate-y-1 hover:shadow-md">
              <div class="flex items-center justify-between">
                <div>
                  <p class="text-base font-semibold text-gray-950">Mickael Rebeu</p>
                  <p class="mt-1 text-sm text-gray-600">Co-fondateur · Web (front/back)</p>
                </div>
                <div class="rounded-2xl bg-sky-50 p-3 text-sky-700 shadow-sm">
                  <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
                  </svg>
                </div>
              </div>
              <ul class="mt-5 space-y-2 text-sm text-gray-700">
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-sky-600" />Apps web performantes</li>
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-sky-600" />Architecture & qualité</li>
                <li class="flex items-start gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-sky-600" />Livraison & itérations rapides</li>
              </ul>
            </div>

            <div class="md:col-span-2 rounded-3xl bg-white/85 p-6 shadow-sm ring-1 ring-gray-200/70 backdrop-blur">
              <p class="text-xs font-semibold uppercase tracking-[0.2em] text-gray-500">Notre mission</p>
              <p class="mt-3 text-sm leading-relaxed text-gray-600">
                Transformer vos idées en produits digitaux utiles : un design solide, des choix techniques clean, et une exécution qui tient dans le temps.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>
