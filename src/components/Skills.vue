<template>
  <section id="competences" class="bg-gray-50 py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Compétences</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          Savoir-faire technique
        </h2>
        <p class="text-gray-500 text-sm mt-3 max-w-lg mx-auto">
          Un ensemble de compétences acquises en formation et consolidées en stage, organisées par domaine.
        </p>
      </div>

      <!-- Grille de catégories -->
      <div class="grid md:grid-cols-2 xl:grid-cols-3 gap-5 max-w-5xl mx-auto">
        <div
          v-for="category in skillCategories"
          :key="category.id"
          data-aos="fade-up"
          class="bg-white rounded-2xl border border-gray-100 p-7 hover:border-primary/20 hover:shadow-md transition-all duration-300"
        >
          <!-- Icône + titre -->
          <div class="flex items-center gap-3 mb-5">
            <div class="w-9 h-9 rounded-lg bg-primary/10 flex items-center justify-center flex-shrink-0">
              <span v-html="category.icon" class="text-primary"></span>
            </div>
            <h3 class="font-semibold text-gray-800 text-sm">{{ category.name }}</h3>
          </div>

          <!-- Tags -->
          <div class="flex flex-wrap gap-2">
            <span
              v-for="skill in category.skills"
              :key="skill.name"
              translate="no"
              class="text-xs px-3 py-1.5 rounded-full border transition-colors"
              :class="skill.primary
                ? 'bg-primary/8 border-primary/25 text-primary font-medium'
                : 'bg-gray-50 border-gray-100 text-gray-600'"
            >
              {{ skill.name }}
            </span>
          </div>
        </div>
      </div>

      <!-- Outils transversaux -->
      <div class="mt-10 max-w-5xl mx-auto bg-white rounded-2xl border border-gray-100 p-7" data-aos="fade-up">
        <h3 class="font-semibold text-gray-700 text-sm mb-4">Outils & environnements</h3>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="tool in transversal"
            :key="tool"
            translate="no"
            class="text-xs text-gray-500 bg-gray-50 border border-gray-100 px-3 py-1.5 rounded-full"
          >
            {{ tool }}
          </span>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const skillCategories = ref([
  {
    id: 1,
    name: 'Conception & Architecture',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M9 9h6M9 12h6M9 15h4"/></svg>`,
    skills: [
      { name: 'MERISE', primary: true },
      { name: 'UML', primary: true },
      { name: 'Ingénierie des besoins', primary: true },
      { name: 'Modélisation SI', primary: false },
      { name: 'Cahier des charges', primary: false },
    ],
  },
  {
    id: 2,
    name: 'Développement Frontend',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>`,
    skills: [
      { name: 'Vue.js 3', primary: true },
      { name: 'Nuxt.js', primary: true },
      { name: 'Pinia', primary: true },
      { name: 'Tailwind CSS', primary: false },
      { name: 'React', primary: false },
      { name: 'JavaScript', primary: false },
      { name: 'HTML / CSS', primary: false },
    ],
  },
  {
    id: 3,
    name: 'Développement Backend & Mobile',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>`,
    skills: [
      { name: 'Node.js', primary: true },
      { name: 'Express.js', primary: false },
      { name: 'Symfony', primary: true },
      { name: 'Flutter', primary: true },
      { name: 'Python', primary: false },
      { name: 'PHP', primary: false },
      { name: 'Dart', primary: false },
    ],
  },
  {
    id: 4,
    name: 'Données & Intelligence Artificielle',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="3"/><path d="M12 1v4M12 19v4M4.22 4.22l2.83 2.83M16.95 16.95l2.83 2.83M1 12h4M19 12h4"/></svg>`,
    skills: [
      { name: 'TensorFlow', primary: true },
      { name: 'PyTorch', primary: false },
      { name: 'Teachable Machine', primary: false },
      { name: 'Flask', primary: false },
      { name: 'Jupyter Notebook', primary: false },
      { name: 'MySQL', primary: false },
      { name: 'PostgreSQL', primary: false },
      { name: 'MongoDB', primary: false },
    ],
  },
  {
    id: 5,
    name: 'Qualité & Tests',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h11"/></svg>`,
    skills: [
      { name: 'Vitest', primary: true },
      { name: 'Cypress', primary: true },
      { name: 'Tests unitaires', primary: false },
      { name: 'Tests E2E', primary: false },
    ],
  },
  {
    id: 6,
    name: 'UI/UX & Design',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 19l7-7 3 3-7 7-3-3z"/><path d="M18 13l-1.5-7.5L2 2l3.5 14.5L13 18l5-5z"/><circle cx="11" cy="11" r="2"/></svg>`,
    skills: [
      { name: 'Figma', primary: true },
      { name: 'Wireframing', primary: false },
      { name: 'Maquettes haute fidélité', primary: false },
      { name: 'Design System', primary: false },
      { name: 'Prototype cliquable', primary: false },
    ],
  },
]);

const transversal = ref([
  'Git', 'GitHub', 'GitLab', 'VS Code', 'Linux', 'Mac OS', 'Windows',
  'REST API', 'GraphQL (notions)', 'JWT', 'Bash',
  'Three.js', 'Processing', 'Qt Creator',
]);
</script>
