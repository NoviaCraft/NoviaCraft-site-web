<template>
  <section class="relative flex min-h-svh flex-col overflow-hidden bg-white pt-28">
    <div class="pointer-events-none absolute inset-0">
      <div class="absolute inset-0 bg-cadrillage" />
      <div class="absolute -top-24 left-1/2 h-80 w-80 -translate-x-1/2 rounded-full bg-emerald-200/40 blur-3xl" />
      <div class="absolute -bottom-28 -left-10 h-80 w-80 rounded-full bg-sky-200/40 blur-3xl" />
    </div>

    <div class="relative mx-auto flex w-full flex-1 items-center max-w-screen-2xl px-2 py-10 sm:px-4 lg:px-6">
      <div class="grid w-full items-center gap-10 lg:grid-cols-2">
        <div class="space-y-6 lg:pr-4">
          <div class="inline-flex items-center gap-2 rounded-full bg-white/80 px-3 py-1 text-xs font-semibold text-gray-700 shadow-sm ring-1 ring-gray-200/70">
            <span class="h-1.5 w-1.5 rounded-full bg-emerald-600" />
            NovIACraft · Agence Web et IA
          </div>
          <h1 class="text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl md:text-6xl leading-tight">
            <span class="block bg-linear-to-r from-sky-500 to-emerald-500 bg-clip-text text-transparent">
              NovIACraft
            </span>
            <span class="block">
              Des produits
              <span class="text-emerald-600"> web & IA</span>
              complets et prêts à l'emploi.
            </span>
          </h1>
          <p class="max-w-2xl text-lg leading-relaxed text-gray-600">
            Sites, applications, solutions data et d'intelligence artificielle.
            Une exécution propre, une performance solide et des résultats mesurables.
          </p>

          <div class="flex flex-col gap-3 sm:flex-row">
            <a
              href="#contact"
              class="inline-flex items-center justify-center rounded-full bg-linear-to-r from-gray-900 to-gray-800 px-7 py-3 text-sm font-semibold text-white shadow-sm hover:from-gray-800 hover:to-gray-700 transition"
            >
              Demander un devis
            </a>
            <a
              href="#realisations"
              class="inline-flex items-center justify-center rounded-full bg-white/85 px-7 py-3 text-sm font-semibold text-gray-900 shadow-sm hover:bg-white transition ring-1 ring-gray-200/70"
            >
              Voir nos réalisations
            </a>
          </div>
        </div>

        <div class="flex items-center justify-center">
          <div class="relative w-full max-w-lg">
            <div class="absolute -left-10 -top-8 h-36 w-36 rounded-full bg-emerald-200/30 blur-3xl" />
            <div class="absolute -right-8 bottom-0 h-36 w-36 rounded-full bg-sky-200/25 blur-3xl" />

            <div class="relative border border-rounded px-4 py-4 border-gray-200/70 pl-10 bg-emerald-50/20">
              <div class="flex items-center justify-between text-[12px] font-semibold uppercase tracking-[0.24em] text-gray-500">
                <span>En chiffres</span>
                <span>{{ currentIndex + 1 }} / {{ stats.length }}</span>
              </div>

              <div class="relative mt-7 h-40 overflow-hidden">
                <transition name="fade-slide" mode="out-in">
                  <div
                    :key="activeStat.label"
                    class="absolute inset-0 flex flex-col items-center justify-center gap-2"
                  >
                    <p class="text-[12px] uppercase tracking-[0.3em] text-gray-500">{{ activeStat.label }}</p>
                    <p class="text-7xl font-semibold text-gray-950 leading-none">{{ activeStat.value }}</p>
                    <p class="text-[15px] text-gray-600">{{ activeStat.caption }}</p>
                  </div>
                </transition>
              </div>

              <div class="mt-7 flex items-center gap-6">
                <div class="flex items-center gap-2">
                  <button
                    v-for="(item, idx) in stats"
                    :key="item.label"
                    class="h-2 w-6 rounded-full transition"
                    :class="idx === currentIndex ? 'bg-emerald-500' : 'bg-gray-300'"
                    @click="goTo(idx)"
                    aria-label="Aller à la statistique"
                  />
                </div>
                <div class="ml-auto flex items-center gap-4 text-[12px] font-semibold uppercase tracking-[0.2em] text-gray-500">
                  <button class="hover:text-gray-900" @click="prevSlide">Préc</button>
                  <span class="text-gray-300">/</span>
                  <button class="hover:text-gray-900" @click="nextSlide">Suiv</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="pointer-events-none absolute bottom-6 left-1/2 -translate-x-1/2">
      <div class="flex flex-col items-center gap-2 text-xs font-semibold uppercase tracking-[0.2em] text-gray-400">
        <span>Scroll</span>
        <span class="relative h-8 w-5 rounded-full border border-gray-300">
          <span class="absolute left-1/2 top-2 h-1.5 w-1.5 -translate-x-1/2 rounded-full bg-gray-400 animate-bounce" />
        </span>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { computed, onBeforeUnmount, onMounted, ref } from 'vue'

const stats = [
  { label: 'Clients', value: '6', caption: 'Accompagnés avec succès' },
  { label: 'Produits livrés', value: '5', caption: 'Projets menés de bout en bout' },
  { label: 'Nos produits', value: '1', caption: 'Solutions maison prêtes à déployer' },
]

const currentIndex = ref(0)
const activeStat = computed(() => stats[currentIndex.value] ?? stats[0]!)

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % stats.length
}

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + stats.length) % stats.length
}

const goTo = (idx: number) => {
  currentIndex.value = idx % stats.length
}

let timer: ReturnType<typeof setInterval> | undefined

onMounted(() => {
  timer = setInterval(nextSlide, 3200)
})

onBeforeUnmount(() => {
  if (timer) clearInterval(timer)
})
</script>
