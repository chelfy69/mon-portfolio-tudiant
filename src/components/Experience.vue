<template>
  <section id="experiences" class="bg-white py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Expériences</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          Stages professionnels
        </h2>
        <p class="text-gray-500 text-sm mt-3 max-w-lg mx-auto">
          Trois expériences en entreprise qui ont structuré ma progression technique et renforcé ma pratique du développement en contexte réel.
        </p>
      </div>

      <!-- Timeline -->
      <div class="max-w-3xl mx-auto relative">
        <!-- Ligne verticale -->
        <div class="absolute left-6 md:left-8 top-4 bottom-4 w-px bg-gray-100 hidden sm:block"></div>

        <div class="space-y-8">
          <div
            v-for="exp in experiences"
            :key="exp.id"
            data-aos="fade-up"
            class="relative flex gap-6 md:gap-10"
          >
            <!-- Dot timeline -->
            <div class="hidden sm:flex flex-col items-center flex-shrink-0">
              <div class="w-4 h-4 rounded-full mt-1 border-2 z-10 flex-shrink-0" :class="exp.id === 1 ? 'border-primary bg-primary' : 'border-gray-300 bg-white'"></div>
            </div>

            <!-- Carte -->
            <div class="flex-1 bg-white rounded-2xl border border-gray-100 p-7 hover:border-primary/20 hover:shadow-md transition-all duration-300 group">
              <!-- Header -->
              <div class="flex flex-col sm:flex-row sm:items-start sm:justify-between gap-2 mb-4">
                <div>
                  <h3 class="font-bold text-gray-900 text-base">{{ exp.role }}</h3>
                  <p class="text-primary text-sm font-medium mt-0.5">{{ exp.company }}</p>
                </div>
                <span class="text-xs text-gray-400 bg-gray-50 border border-gray-100 px-3 py-1.5 rounded-full whitespace-nowrap self-start">
                  {{ exp.period }}
                </span>
              </div>

              <!-- Description -->
              <p class="text-gray-500 text-sm leading-relaxed mb-4">{{ exp.description }}</p>

              <!-- Missions -->
              <ul class="space-y-1.5 mb-4">
                <li
                  v-for="task in exp.tasks"
                  :key="task"
                  class="flex items-start gap-2 text-sm text-gray-600"
                >
                  <span class="w-1.5 h-1.5 rounded-full bg-primary/60 flex-shrink-0 mt-1.5"></span>
                  {{ task }}
                </li>
              </ul>

              <!-- Stack -->
              <div class="flex flex-wrap gap-2 pt-3 border-t border-gray-50">
                <span
                  v-for="tech in exp.stack"
                  :key="tech"
                  translate="no"
                  class="text-xs text-gray-500 bg-gray-50 border border-gray-100 px-2.5 py-1 rounded-md"
                >
                  {{ tech }}
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
const experiences = ref([
  {
    id: 1,
    role: 'Stagiaire Développeur Web Junior',
    company: 'TechSolution Bénin',
    period: 'Mars – Juin 2025',
    description: 'Développement d\'une application de gestion interne en équipe. Prise en main d\'un environnement de production, intégration de maquettes et contribution aux processus qualité.',
    tasks: [
      'Développement d\'une application de gestion interne (Node.js, Vue.js, MySQL)',
      'Intégration de maquettes Figma et optimisation de l\'interface utilisateur',
      'Correction de bugs et rédaction de tests unitaires',
      'Collaboration en équipe et participation aux revues de code',
    ],
    stack: ['Vue.js', 'Node.js', 'MySQL', 'Figma', 'Git'],
  },
  {
    id: 2,
    role: 'Stagiaire Développeur Full-Stack (Stage académique)',
    company: 'SET-IT Bénin',
    period: 'Avril – Septembre 2023',
    description: 'Stage de soutenance de licence centré sur la conception et le développement complet du projet ALAFIA LIFE — application mobile de suivi nutritionnel avec reconnaissance d\'images par IA.',
    tasks: [
      'Conception et développement mobile complet (Flutter / Dart)',
      'Intégration d\'un pipeline IA côté serveur : photo → API backend → prédiction (TensorFlow / Teachable Machine)',
      'Contribution à l\'API REST (Laravel) et modélisation UML du système',
      'Estimation calorique et recommandations d\'activité physique',
    ],
    stack: ['Flutter', 'Dart', 'Python', 'TensorFlow', 'Flask', 'Laravel', 'MySQL'],
  },
  {
    id: 3,
    role: 'Stagiaire Développeur Frontend',
    company: 'InnovDev Services',
    period: 'Juin – Août 2022',
    description: 'Premier stage professionnel orienté développement frontend, au sein d\'une équipe projet travaillant sur un environnement Symfony.',
    tasks: [
      'Contribution au développement du site web (HTML, CSS, intégration Symfony)',
      'Rédaction de documentation technique',
      'Participation aux réunions de suivi projet',
    ],
    stack: ['HTML', 'CSS', 'Symfony', 'JavaScript'],
  },
]);
</script>
