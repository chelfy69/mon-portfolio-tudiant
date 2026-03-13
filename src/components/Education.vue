<template>
  <section id="formation" class="bg-gray-50 py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Formation</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          Parcours académique
        </h2>
      </div>

      <!-- Timeline -->
      <div class="max-w-3xl mx-auto space-y-6">
        <div
          v-for="(item, index) in educations"
          :key="item.id"
          data-aos="fade-up"
          class="relative bg-white rounded-2xl border border-gray-100 p-8 hover:border-primary/20 hover:shadow-md transition-all duration-300"
        >
          <!-- Badge actuel -->
          <span
            v-if="item.current"
            class="absolute top-6 right-6 text-[10px] font-semibold text-green-600 bg-green-50 border border-green-200 px-2.5 py-1 rounded-full"
          >
            En cours
          </span>

          <div class="flex items-start gap-5">
            <!-- Icône institution -->
            <div class="w-12 h-12 rounded-xl flex items-center justify-center flex-shrink-0" :class="index === 0 ? 'bg-primary/10' : 'bg-gray-100'">
              <svg width="22" height="22" viewBox="0 0 24 24" fill="none" :stroke="index === 0 ? '#0CA7FF' : '#9ca3af'" stroke-width="1.8">
                <path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/>
              </svg>
            </div>

            <div class="flex-1">
              <!-- Diplôme -->
              <h3 class="font-bold text-gray-900 text-base mb-0.5">{{ item.degree }}</h3>
              <!-- Spécialité -->
              <p class="text-primary text-sm font-medium mb-1">{{ item.specialty }}</p>
              <!-- Établissement -->
              <p class="text-gray-500 text-sm mb-1">{{ item.school }}</p>
              <!-- Période -->
              <p class="text-gray-400 text-xs mb-4">{{ item.period }}</p>

              <!-- Points clés -->
              <div class="flex flex-wrap gap-2">
                <span
                  v-for="tag in item.highlights"
                  :key="tag"
                  class="text-xs text-gray-600 bg-gray-50 border border-gray-100 px-3 py-1 rounded-full"
                >
                  {{ tag }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
const educations = ref([
  {
    id: 1,
    degree: 'Licence 3 Informatique',
    specialty: 'Parcours Service Multimédia',
    school: 'UFR STGI — Université Marie & Louis Pasteur, Montbéliard',
    period: 'Septembre 2025 — Présent',
    current: true,
    highlights: [
      'Développement d\'applications web',
      'Conception logicielle',
      'Bases de données & modélisation',
      'Algorithmique géométrique',
      'Imagerie & rendu',
    ],
  },
  {
    id: 2,
    degree: 'Licence — Informatique de Gestion',
    specialty: 'Spécialité Analyste Informatique & Programmation',
    school: 'ENEAM — École Nationale d\'Économie Appliquée et de Management (UAC, Bénin)',
    period: '2020 — 2023',
    current: false,
    highlights: [
      'Analyse & conception de systèmes (MERISE, UML)',
      'Ingénierie des besoins',
      'Bases solides en programmation',
      'Gestion de projet informatique',
    ],
  },
]);
</script>
