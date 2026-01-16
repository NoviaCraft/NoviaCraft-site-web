<template>
  <section id="realisations" class="bg-white py-20">
    <div class="mx-auto max-w-screen-2xl px-2 sm:px-4 lg:px-6">
      <div class="max-w-2xl">
        <p class="flex items-center gap-3 text-xl font-semibold uppercase tracking-[0.28em] text-emerald-600/80">
          <span class="h-px w-10 bg-emerald-400/70" />
          Réalisations
        </p>
        <h2 class="mt-4 text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl leading-tight">
          Du concret, livré et en ligne
        </h2>
        <p class="mt-4 text-lg leading-relaxed text-gray-600">
          Deux projets web (2 portfolios) et une application mobile. Cliquez sur un projet pour voir l'aperçu. D'autres solutions ont été en privé pour des entreprises, contactez-nous pour en discuter ! 
        </p>
      </div>

      <div class="mt-12 grid gap-8 lg:grid-cols-12">
        <div class="lg:col-span-4">
          <div class="space-y-3">
            <button
              v-for="project in projects"
              :key="project.id"
              type="button"
              @click="selectedId = project.id"
              :class="[
                'w-full rounded-2xl px-5 py-4 text-left transition',
                selectedId === project.id
                  ? 'bg-gray-950 text-white shadow-sm'
                  : 'bg-gray-50 text-gray-950 hover:bg-gray-100',
              ]"
            >
              <p
                class="text-xs font-semibold"
                :class="selectedId === project.id ? 'text-white/70' : 'text-gray-500'"
              >
                {{ project.kind }}
              </p>
              <div class="mt-1 flex items-start justify-between gap-3">
                <p class="text-base font-semibold leading-tight">{{ project.name }}</p>
                <svg
                  class="mt-0.5 h-4 w-4"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                  :class="selectedId === project.id ? 'text-white/70' : 'text-gray-400'"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                </svg>
              </div>
              <p
                class="mt-2 text-sm leading-relaxed"
                :class="selectedId === project.id ? 'text-white/75' : 'text-gray-600'"
              >
                {{ project.description }}
              </p>
            </button>
          </div>

          <a
            v-if="selectedProject.url"
            :href="selectedProject.url"
            target="_blank"
            rel="noopener noreferrer"
            class="mt-5 inline-flex items-center gap-2 text-sm font-semibold text-emerald-700 hover:text-emerald-600"
          >
            Ouvrir dans un nouvel onglet
            <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
            </svg>
          </a>
          <p v-if="selectedProject.preview === 'iframe'" class="mt-2 text-xs text-gray-500">
            Si l'aperçu ne s'affiche pas, c'est souvent lié aux protections d'embed (CSP / X-Frame-Options).
          </p>
        </div>

        <div class="lg:col-span-8">
          <div class="rounded-4xl border border-gray-200/80 bg-white/70 p-4 shadow-[0_20px_60px_-40px_rgba(15,23,42,0.35)] backdrop-blur sm:p-6">
            <div class="flex flex-col gap-4 sm:flex-row sm:items-start sm:justify-between">
              <div>
                <p class="text-xs font-semibold uppercase tracking-[0.24em] text-emerald-600/80">
                  {{ selectedProject.preview === 'iframe' ? 'Aperçu (live)' : 'Démo (carousel)' }}
                </p>
                <p class="mt-2 text-base font-semibold text-gray-950">{{ selectedProject.name }}</p>
              </div>
              <div class="flex flex-wrap gap-2">
                <span
                  v-for="tag in selectedProject.tags"
                  :key="tag"
                  class="rounded-full bg-white/80 px-3 py-1 text-xs font-semibold text-gray-700 ring-1 ring-gray-200/80"
                >
                  {{ tag }}
                </span>
              </div>
            </div>

            <div v-if="selectedProject.preview === 'iframe'" class="mt-5 overflow-hidden rounded-2xl bg-white shadow-sm">
              <div class="aspect-16/10 bg-white">
                <iframe
                  :key="selectedProject.id"
                  :title="selectedProject.iframeTitle"
                  :src="selectedProject.url"
                  class="h-full w-full"
                  loading="lazy"
                  referrerpolicy="no-referrer"
                />
              </div>
            </div>

            <div v-else class="mt-6 overflow-hidden rounded-3xl bg-white/80 ring-1 ring-gray-200/80 shadow-[0_16px_45px_-35px_rgba(15,23,42,0.35)]">
              <div class="aspect-16/10 bg-white/90">
                <div class="flex h-full items-center justify-center px-4 py-7 sm:px-6">
                  <div class="flex w-full max-w-140 items-center justify-center gap-4 sm:gap-6">
                    <button
                      type="button"
                      @click="prevSlide"
                      class="hidden sm:inline-flex h-10 w-10 items-center justify-center rounded-full bg-white/90 text-gray-900 ring-1 ring-gray-200/80 hover:ring-gray-300"
                      aria-label="Écran précédent"
                    >
                      <svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                      </svg>
                    </button>

                    <div class="flex w-full max-w-[320px] flex-col items-center gap-4">
                      <div class="relative w-full overflow-hidden rounded-[2.5rem] bg-white shadow-[0_18px_50px_-40px_rgba(15,23,42,0.45)] ring-1 ring-gray-100">
                        <div class="absolute inset-x-0 top-3 mx-auto h-5 w-24 rounded-full bg-gray-900/10" />
                        <div class="aspect-9/19 bg-gray-50">
                          <img
                            :src="todoImages[currentSlide]"
                            :alt="`ToDo App – écran ${currentSlide + 1}`"
                            class="h-full w-full object-contain"
                          />
                        </div>
                      </div>

                      <div class="flex items-center gap-2">
                        <button
                          v-for="(_, i) in todoImages"
                          :key="i"
                          type="button"
                          @click="goToSlide(i)"
                          :class="[
                            'h-2 w-6 rounded-full transition',
                            i === currentSlide ? 'bg-emerald-500' : 'bg-gray-300 hover:bg-gray-400',
                          ]"
                          :aria-label="`Aller à l'écran ${i + 1}`"
                        />
                      </div>
                    </div>

                    <button
                      type="button"
                      @click="nextSlide"
                      class="hidden sm:inline-flex h-10 w-10 items-center justify-center rounded-full bg-white/90 text-gray-900 ring-1 ring-gray-200/80 hover:ring-gray-300"
                      aria-label="Écran suivant"
                    >
                      <svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                      </svg>
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';

import todoImage1 from '../assets/todo.png';
import todoImage2 from '../assets/todo2.png';
import todoImage3 from '../assets/todo3.png';
import todoImage4 from '../assets/todo4.png';
import todoImage5 from '../assets/todo5.png';

type Project = {
  id: string;
  kind: string;
  name: string;
  url?: string;
  description: string;
  tags: string[];
  preview: 'iframe' | 'carousel';
  iframeTitle?: string;
};

const projects: Project[] = [
  {
    id: 'jonathan',
    kind: 'Portfolio',
    name: 'Jonathan Steuer',
    url: 'https://www.jonathansteuer.fr/',
    description: "Site créatif : structure claire, navigation fluide et rendu soigné.",
    tags: ['Design', 'Responsive', 'Créatif'],
    preview: 'iframe',
    iframeTitle: 'Aperçu portfolio Jonathan Steuer',
  },
  {
    id: 'tdne',
    kind: 'Portfolio',
    name: 'TDNE',
    url: 'https://tdne.netlify.app/',
    description: "Site Bento : visuels, rythme et mise en valeur des projets.",
    tags: ['Performance', 'Bento', 'Visuels'],
    preview: 'iframe',
    iframeTitle: 'Aperçu portfolio TDNE',
  },
  {
    id: 'todo',
    kind: 'App mobile',
    name: 'To-Do List',
    description: 'Démo en screenshots : navigation simple, listes de tâches et interactions rapides.',
    tags: ['Mobile', 'UI/UX', 'Productivité', 'To-do'],
    preview: 'carousel',
  },
];

const selectedId = ref(projects[0]!.id);
const selectedProject = computed<Project>(() => projects.find((p) => p.id === selectedId.value) ?? projects[0]!);

const todoImages = [todoImage1, todoImage2, todoImage3, todoImage4, todoImage5];
const currentSlide = ref(0);

const prevSlide = () => {
  currentSlide.value = (currentSlide.value + todoImages.length - 1) % todoImages.length;
};

const nextSlide = () => {
  currentSlide.value = (currentSlide.value + 1) % todoImages.length;
};

const goToSlide = (index: number) => {
  if (index < 0 || index >= todoImages.length) return;
  currentSlide.value = index;
};
</script>
