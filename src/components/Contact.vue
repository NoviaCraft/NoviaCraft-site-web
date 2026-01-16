<template>
  <section id="contact" class="bg-gray-50 py-20">
    <div class="mx-auto max-w-screen-2xl px-2 sm:px-4 lg:px-6">
      <div class="grid gap-10 lg:grid-cols-12">
        <div class="lg:col-span-5">
          <p class="flex items-center gap-3 text-xl font-semibold uppercase tracking-[0.28em] text-emerald-600/80">
            <span class="h-px w-10 bg-emerald-400/70" />
            Contact
          </p>
          <h2 class="mt-4 text-4xl font-semibold tracking-tight text-gray-950 sm:text-5xl leading-tight">
            Parlez-nous de votre besoin
          </h2>
          <p class="mt-4 text-lg leading-relaxed text-gray-600">
            Décrivez votre projet (site, app web, data, IA ou CRM). On revient vers vous avec une première recommandation et une estimation.
          </p>

          <div class="mt-8 rounded-2xl bg-white p-6 shadow-sm">
            <p class="text-sm font-semibold text-gray-950">Ce qu'on vous demande</p>
            <ul class="mt-3 space-y-2 text-sm text-gray-600">
              <li class="flex gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />Objectif + contexte</li>
              <li class="flex gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />Délais souhaités</li>
              <li class="flex gap-3"><span class="mt-2 h-1.5 w-1.5 rounded-full bg-emerald-600" />Budget (même approximatif)</li>
            </ul>
          </div>
        </div>

        <div class="lg:col-span-7">
          <div class="rounded-3xl bg-white p-6 shadow-sm sm:p-8">
            <form class="space-y-5">
              <div class="grid gap-5 sm:grid-cols-2">
                <div>
                  <label for="nom" class="block text-sm font-semibold text-gray-900">Nom</label>
                  <input
                    type="text"
                    id="nom"
                    class="mt-2 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 text-sm text-gray-900 placeholder:text-gray-400 focus:outline-none focus:ring-2 focus:ring-emerald-500"
                    placeholder="Votre nom"
                  />
                </div>
                <div>
                  <label for="email" class="block text-sm font-semibold text-gray-900">Email</label>
                  <input
                    type="email"
                    id="email"
                    class="mt-2 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 text-sm text-gray-900 placeholder:text-gray-400 focus:outline-none focus:ring-2 focus:ring-emerald-500"
                    placeholder="votre@email.com"
                  />
                </div>
              </div>

              <div>
                <label for="entreprise" class="block text-sm font-semibold text-gray-900">Entreprise</label>
                <input
                  type="text"
                  id="entreprise"
                  class="mt-2 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 text-sm text-gray-900 placeholder:text-gray-400 focus:outline-none focus:ring-2 focus:ring-emerald-500"
                  placeholder="Nom de votre entreprise"
                />
              </div>

              <div>
                <label for="service" class="block text-sm font-semibold text-gray-900">Sujet</label>
                <select
                  id="service"
                  class="mt-2 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 text-sm text-gray-900 focus:outline-none focus:ring-2 focus:ring-emerald-500"
                >
                  <option value="">Sélectionnez un sujet</option>
                  <option value="site-web">Site Web</option>
                  <option value="app-web">Application Web</option>
                  <option value="ia">IA</option>
                  <option value="data">Analyse de Données</option>
                  <option value="crm">CRM</option>
                  <option value="autre">Autre</option>
                </select>
              </div>

              <div>
                <label for="message" class="block text-sm font-semibold text-gray-900">Message</label>
                <textarea
                  id="message"
                  rows="6"
                  class="mt-2 w-full rounded-xl border border-gray-300 bg-white px-4 py-3 text-sm text-gray-900 placeholder:text-gray-400 focus:outline-none focus:ring-2 focus:ring-emerald-500"
                  placeholder="Contexte, objectif, fonctionnalités, délais..."
                ></textarea>
              </div>

              <div class="flex flex-col gap-3 sm:flex-row sm:items-center sm:justify-between">
                <p class="text-xs text-gray-500">Réponse sous 24–48h ouvrées.</p>
                <button
                  type="submit"
                  class="inline-flex items-center justify-center rounded-full bg-gray-900 px-7 py-3 text-sm font-semibold text-white shadow-sm hover:bg-gray-800 transition"
                >
                  Envoyer
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>
