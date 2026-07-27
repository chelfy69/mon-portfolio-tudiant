<template>
  <section id="experiences" class="bg-white py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Expériences</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          En entreprise
        </h2>
        <p class="text-gray-500 text-sm mt-3 max-w-lg mx-auto">
          Quatre stages, du premier passage en équipe frontend à une plateforme d'apprentissage développée dans un laboratoire de recherche. C'est là que j'ai appris à travailler avec d'autres développeurs.
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
    role: 'Stagiaire Développeur Full-Stack',
    company: 'Institut FEMTO-ST, Montbéliard',
    period: 'Mars à juin 2026',
    description: 'Mon stage de fin de Licence 3, dans un laboratoire de recherche français. J\'ai développé toute la partie enseignant de TaAlam, une plateforme d\'apprentissage en ligne destinée aux établissements scolaires.',
    tasks: [
      'Développement de l\'espace enseignant : création de cours, modules et leçons',
      'Parcours de création en quatre étapes, avec une validation complète avant publication',
      'Mise en place des quiz, des devoirs et du suivi de progression des étudiants',
      'Interfaces construites avec Blade, Tailwind CSS et Alpine.js sur une base Laravel 11',
    ],
    stack: ['Laravel 11', 'Blade', 'Tailwind CSS', 'Alpine.js', 'MySQL', 'Git'],
  },
  {
    id: 2,
    role: 'Stagiaire Développeur Web Junior',
    company: 'TechSolution Bénin',
    period: 'Mars à juin 2025',
    description: 'Développement d\'une application de gestion interne au sein d\'une équipe. Mon premier contact avec un environnement de production, avec tout ce que ça implique : maquettes à intégrer, bugs à corriger et code relu par les autres.',
    tasks: [
      'Développement d\'une application de gestion interne (Node.js, Vue.js, MySQL)',
      'Intégration de maquettes Figma et optimisation de l\'interface utilisateur',
      'Correction de bugs et rédaction de tests unitaires',
      'Collaboration en équipe et participation aux revues de code',
    ],
    stack: ['Vue.js', 'Node.js', 'MySQL', 'Figma', 'Git'],
  },
  {
    id: 3,
    role: 'Stagiaire Développeur Full-Stack',
    company: 'SET-IT Bénin',
    period: 'Mars à septembre 2023',
    description: 'Mon stage de fin de licence au Bénin, sur lequel j\'ai conçu et développé ALAFIA LIFE : une application mobile de suivi nutritionnel qui reconnaît un plat à partir d\'une photo. J\'ai tout porté, de la modélisation au modèle de reconnaissance.',
    tasks: [
      'Conception et développement mobile complet (Flutter / Dart)',
      'Mise en place du pipeline côté serveur : la photo part vers l\'API, le modèle la reconnaît et renvoie le résultat (TensorFlow / Teachable Machine)',
      'Contribution à l\'API REST (Laravel) et modélisation UML du système',
      'Estimation calorique et recommandations d\'activité physique',
    ],
    stack: ['Flutter', 'Dart', 'Python', 'TensorFlow', 'Flask', 'Laravel', 'MySQL'],
  },
  {
    id: 4,
    role: 'Stagiaire Développeur Frontend',
    company: 'InnovDev Services',
    period: 'Mai à août 2022',
    description: 'Mon tout premier stage. J\'ai rejoint une équipe qui travaillait sous Symfony et je me suis occupé de la partie frontend du site, en apprenant sur le tas comment un projet avance au quotidien.',
    tasks: [
      'Contribution au développement du site web (HTML, CSS, intégration Symfony)',
      'Rédaction de documentation technique',
      'Participation aux réunions de suivi projet',
    ],
    stack: ['HTML', 'CSS', 'Symfony', 'JavaScript'],
  },
]);
</script>
