<template>
  <section id="profil" class="bg-white py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="max-w-2xl mb-16" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Profil</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight mb-5">
          Qui je suis
        </h2>
        <p class="text-gray-500 text-[15px] leading-relaxed">
          J'ai commencé l'informatique au Bénin, dans une école où on m'a appris à analyser un besoin
          avant d'écrire la première ligne de code : MERISE, UML, cahier des charges. Depuis mon arrivée
          en France, j'ai surtout fait du web full-stack, avec Vue.js côté interface et Laravel, Node.js
          ou Symfony côté serveur. Mon dernier stage, à l'Institut FEMTO-ST, m'a fait construire l'espace
          enseignant d'une plateforme d'apprentissage complète. Ce que j'aime, c'est suivre un produit
          du début à la fin, de la maquette Figma jusqu'à la mise en ligne, et comprendre à qui il sert vraiment.
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

      <!-- Recherche d'alternance -->
      <div class="mt-14 p-8 rounded-2xl bg-primary/5 border border-primary/15" data-aos="fade-up">
        <div class="flex items-start gap-5">
          <div class="w-10 h-10 rounded-xl bg-primary flex items-center justify-center flex-shrink-0 mt-0.5">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
              <rect x="2" y="7" width="20" height="14" rx="2"/>
              <path d="M16 21V5a2 2 0 00-2-2h-4a2 2 0 00-2 2v16"/>
            </svg>
          </div>
          <div>
            <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-2">Ce que je cherche</p>
            <p class="text-gray-700 text-sm leading-relaxed font-medium">
              Une <strong>alternance en développement web full-stack ou en conception de produit web</strong>,
              à partir de la rentrée de septembre 2026 et pour toute la durée de mon master.
              Je suis prêt à m'installer n'importe où en France. Ce qui compte pour moi : rejoindre une équipe
              où je peux prendre une fonctionnalité en charge du début à la fin, apprendre les habitudes
              de travail d'une vraie entreprise, et rendre du code qu'un collègue pourra reprendre sans moi.
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
    title: 'Analyse & conception produit',
    description: 'Traduire un besoin flou en quelque chose de constructible : MERISE, UML, cahier des charges. Je préfère cadrer avant de coder.',
  },
  {
    id: 2,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>`,
    title: 'Développement Full-Stack',
    description: 'Vue.js 3, Nuxt.js, Laravel, Node.js, Symfony, APIs REST. Je suis à l\'aise des deux côtés, de la maquette jusqu\'au déploiement.',
  },
  {
    id: 3,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="3"/><path d="M12 1v4M12 19v4M4.22 4.22l2.83 2.83M16.95 16.95l2.83 2.83M1 12h4M19 12h4M4.22 19.78l2.83-2.83M16.95 7.05l2.83-2.83"/></svg>`,
    title: 'Data & Intelligence Artificielle',
    description: 'Brancher un modèle TensorFlow dans une vraie application, nettoyer et exploiter des données avec Python. Deux projets menés là-dessus.',
  },
  {
    id: 4,
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h11"/></svg>`,
    title: 'Qualité & Tests',
    description: 'Tests unitaires avec Vitest, tests bout en bout avec Cypress, revues de code. Livrer quelque chose qui tient dans la durée.',
  },
]);
</script>
