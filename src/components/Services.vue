<template>
  <section id="profil" class="bg-white py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="max-w-2xl mb-16" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Profil</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight mb-5">
          Parcours &amp; orientation académique
        </h2>
        <p class="text-gray-500 text-[15px] leading-relaxed">
          Étudiant en Licence 3 Informatique, je m'oriente vers l'ingénierie logicielle
          avec un intérêt particulier pour la conception de systèmes robustes et maintenables,
          ainsi que pour les problématiques liées à la donnée et à l'intelligence artificielle.
          Mon parcours, entre le Bénin et la France, m'a permis de consolider des bases solides
          en développement full-stack, en modélisation de systèmes (UML, MERISE) et en qualité logicielle.
          Je souhaite aujourd'hui approfondir l'architecture applicative et l'intégration de briques
          data/IA dans des produits complets et fiables.
        </p>
      </div>

      <!-- Domaines d'intérêt -->
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-5">
        <div
          v-for="domain in domains"
          :key="domain.id"
          data-aos="fade-up"
          class="group p-6 rounded-2xl border border-gray-100 bg-gray-50 hover:bg-white hover:border-primary/20 hover:shadow-lg transition-all duration-300"
        >
          <div class="w-10 h-10 rounded-xl bg-primary/10 flex items-center justify-center mb-4 group-hover:bg-primary/15 transition-colors">
            <span v-html="domain.icon" class="text-primary"></span>
          </div>
          <h3 class="font-semibold text-gray-800 text-sm mb-2">{{ domain.title }}</h3>
          <p class="text-gray-500 text-xs leading-relaxed">{{ domain.description }}</p>
        </div>
      </div>

      <!-- Objectif académique -->
      <div class="mt-14 p-8 rounded-2xl bg-primary/5 border border-primary/15" data-aos="fade-up">
        <div class="flex items-start gap-5">
          <div class="w-10 h-10 rounded-xl bg-primary flex items-center justify-center flex-shrink-0 mt-0.5">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
              <path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/>
            </svg>
          </div>
          <div>
            <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-2">Objectif académique</p>
            <p class="text-gray-700 text-sm leading-relaxed font-medium">
              Poursuivre vers une spécialisation en <strong>Ingénierie Logicielle</strong> afin d'approfondir
              la conception d'architectures robustes, les méthodes de validation et de qualité,
              ainsi que les problématiques de performance, scalabilité et maintenabilité.
              Mon objectif est de concevoir des solutions complètes, fiables et évolutives,
              intégrant des briques data/IA là où cela est pertinent.
            </p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
const domains = ref([
  {
    id: 1,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M9 9h6M9 12h6M9 15h4"/></svg>`,
    title: 'Architecture Logicielle',
    description: 'Conception de systèmes modulaires, structuration du code, MERISE et UML, ingénierie des besoins.',
  },
  {
    id: 2,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>`,
    title: 'Développement Full-Stack',
    description: 'Vue.js 3, Nuxt.js, Node.js, Symfony, APIs REST — de l\'architecture au déploiement.',
  },
  {
    id: 3,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="3"/><path d="M12 1v4M12 19v4M4.22 4.22l2.83 2.83M16.95 16.95l2.83 2.83M1 12h4M19 12h4M4.22 19.78l2.83-2.83M16.95 7.05l2.83-2.83"/></svg>`,
    title: 'Data &amp; Intelligence Artificielle',
    description: 'Intégration de modèles IA (TensorFlow, PyTorch), pipelines de traitement de données, orchestration de services.',
  },
  {
    id: 4,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h11"/></svg>`,
    title: 'Qualité &amp; Tests',
    description: 'Tests unitaires (Vitest), tests E2E (Cypress), structuration du code, bonnes pratiques de développement.',
  },
]);
</script>
