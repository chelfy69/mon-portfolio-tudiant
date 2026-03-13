<template>
  <section id="projects" class="bg-white py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Projets</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          Réalisations &amp; études de cas
        </h2>
        <p class="text-gray-500 text-sm mt-3 max-w-lg mx-auto">
          Projets académiques et personnels illustrant ma progression, ma démarche et mes choix techniques.
        </p>
      </div>

      <!-- Grille projets -->
      <div class="grid md:grid-cols-2 gap-7 max-w-5xl mx-auto">
        <div
          v-for="project in projects"
          :key="project.id"
          data-aos="fade-up"
          class="group rounded-2xl border border-gray-100 bg-white overflow-hidden hover:border-primary/20 hover:shadow-xl transition-all duration-300 hover:-translate-y-1 flex flex-col"
        >
          <!-- Browser bar + screenshot -->
          <div class="relative overflow-hidden">
            <div class="flex items-center gap-1.5 px-4 py-3 bg-gray-50 border-b border-gray-100">
              <span class="w-2.5 h-2.5 rounded-full bg-red-400/70"></span>
              <span class="w-2.5 h-2.5 rounded-full bg-yellow-400/70"></span>
              <span class="w-2.5 h-2.5 rounded-full bg-green-400/70"></span>
              <div class="ml-3 flex-1 bg-white rounded px-3 py-1 text-xs text-gray-400 truncate border border-gray-200">
                {{ project.context }}
              </div>
              <a
                v-if="project.gitURL"
                :href="project.gitURL"
                target="_blank"
                rel="noopener noreferrer"
                class="ml-2 flex items-center gap-1 text-xs text-gray-400 hover:text-primary transition-colors flex-shrink-0"
              >
                <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
                </svg>
                Code
              </a>
            </div>
            <div class="screenshot-wrapper relative">
              <img
                :src="project.image"
                :alt="project.title"
                class="w-full h-48 object-cover object-top transition-transform duration-500 group-hover:scale-[1.03]"
              />
              <div class="screenshot-overlay absolute inset-0 bg-primary/65 flex items-center justify-center opacity-0 transition-opacity duration-300">
                <a
                  v-if="project.liveURL"
                  :href="project.liveURL"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="flex items-center gap-2 bg-white text-primary font-medium text-sm px-5 py-2.5 rounded-full hover:bg-primary hover:text-white transition-all"
                >
                  <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
                    <path d="M18 13v6a2 2 0 01-2 2H5a2 2 0 01-2-2V8a2 2 0 012-2h6"/>
                    <polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/>
                  </svg>
                  Voir le projet
                </a>
              </div>
            </div>
          </div>

          <!-- Contenu -->
          <div class="p-6 flex flex-col flex-1">
            <div class="flex items-center gap-2 mb-3">
              <span class="text-xs font-medium text-primary bg-primary/8 border border-primary/20 px-2.5 py-1 rounded-full">
                {{ project.category }}
              </span>
              <span v-if="project.year" class="text-xs text-gray-400">{{ project.year }}</span>
            </div>
            <h3 class="font-bold text-gray-900 text-base mb-2">{{ project.title }}</h3>
            <p class="text-gray-500 text-sm leading-relaxed line-clamp-3 mb-4">{{ project.description }}</p>
            <div class="flex flex-wrap gap-1.5 mb-5">
              <span
                v-for="tech in project.stack"
                :key="tech"
                translate="no"
                class="text-xs text-gray-500 bg-gray-50 border border-gray-100 px-2 py-1 rounded-md"
              >{{ tech }}</span>
            </div>
            <div class="flex items-center gap-3 mt-auto pt-4 border-t border-gray-50">
              <a
                v-if="project.liveURL"
                :href="project.liveURL"
                target="_blank"
                rel="noopener noreferrer"
                class="flex-1 flex items-center justify-center gap-2 bg-primary text-white text-xs font-medium px-4 py-2.5 rounded-xl hover:bg-primary/90 transition-all hover:-translate-y-0.5"
              >
                <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
                  <circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/>
                  <path d="M12 2a15.3 15.3 0 014 10 15.3 15.3 0 01-4 10 15.3 15.3 0 01-4-10 15.3 15.3 0 014-10z"/>
                </svg>
                Live / App Store
              </a>
              <a
                v-if="project.gitURL"
                :href="project.gitURL"
                target="_blank"
                rel="noopener noreferrer"
                class="flex items-center justify-center gap-2 border border-gray-200 text-gray-600 text-xs font-medium px-4 py-2.5 rounded-xl hover:border-primary hover:text-primary transition-all hover:-translate-y-0.5"
                :class="!project.liveURL ? 'flex-1' : ''"
              >
                <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
                </svg>
                Code source
              </a>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const projects = ref([
  {
    id: 1,
    image: '/luxe.png',
    title: 'LUXE Collection — E-Commerce Full-Stack',
    category: 'Projet de cours',
    year: '2026',
    context: 'Programmation Web Avancée · Vue 3 + Node.js',
    description: 'Plateforme e-commerce full-stack avec API REST sécurisée et interface "luxury dark". Catalogue produits, panier persistant, checkout, espace client et dashboard admin avec gestion des stocks et des commandes.',
    stack: ['Vue 3', 'Pinia', 'Vue Router', 'Vite', 'Axios', 'Node.js', 'Express', 'JWT', 'bcrypt', 'SQLite'],
    gitURL: 'https://gitlab.com/Chelfy22/luxe',
    liveURL: '',
  },
  {
    id: 2,
    image: '/voyazen.png',
    title: 'VoyaZen — Application Full-Stack',
    category: 'Projet académique',
    year: '2026',
    context: 'En cours · Vue.js / Symfony',
    description: 'Application modulaire avec algorithme de comparaison basé sur filtrage dynamique et scoring de correspondance. UI conçue sur Figma (prototype cliquable + design system) puis intégrée en responsive avec tests unitaires.',
    stack: ['Vue.js', 'Pinia', 'Tailwind CSS', 'Vitest', 'Symfony', 'MySQL'],
    gitURL: 'https://gitlab.com/Chelfy22/voyazen-front',
    liveURL: '',
  },
  {
    id: 3,
    image: '/parent.jpg',
    title: 'Parents d\'à côté — Application Mobile',
    category: 'Produit publié',
    year: '2024',
    context: 'App Store · Flutter / Dart',
    description: 'Application d\'entraide locale entre familles pour la garde d\'enfants. Profils, demandes/offres, messagerie sécurisée, calendrier intégré et parcours "première rencontre".',
    stack: ['Flutter', 'Dart'],
    gitURL: 'https://gitlab.com/rr151/parentdacote-mobile/-/tree/5c40b0f1a7c49ab7d8db93ff4fdb14c2ae7b03ca/',
    liveURL: 'https://apps.apple.com/fr/app/parents-d%C3%A0-c%C3%B4t%C3%A9/id6746669997',
  },
  {
    id: 4,
    image: '/life.png',
    title: 'ALAFIA LIFE — Suivi nutritionnel & IA',
    category: 'Soutenance · Stage SET-IT',
    year: '2023',
    context: 'Stage académique 3 mois · Flutter + Python/IA',
    description: 'Application mobile de suivi nutritionnel avec reconnaissance d\'image par IA : photo d\'un plat → backend Python (TensorFlow / Teachable Machine) → estimation calorique + recommandations sportives.',
    stack: ['Flutter', 'Dart', 'Python', 'TensorFlow', 'Flask', 'Laravel', 'MySQL'],
    gitURL: '',
    liveURL: '',
  },
  {
    id: 5,
    image: '/géométrie.png',
    title: 'Algorithmique Géométrique',
    category: 'Projet académique',
    year: '2025',
    context: 'Géométrie computationnelle · JavaScript + Three.js',
    description: 'Exploration des fondements de la géométrie computationnelle : primitives (Point, Segment, Polygon), opérations fondamentales (orientation, distances, intersections) et visualisation interactive 2D/3D.',
    stack: ['JavaScript', 'Three.js'],
    gitURL: '',
    liveURL: '',
  },
  {
    id: 6,
    image: '/ia.png',
    title: 'Générateur d\'Images par IA',
    category: 'Projet personnel',
    year: '2025',
    context: 'IA générative · JavaScript Vanilla',
    description: 'Application web d\'amélioration de prompts et génération d\'images via plusieurs APIs (Pollinations, Stable Diffusion, Hugging Face) avec fallback automatique, historique et galerie.',
    stack: ['JavaScript', 'HTML', 'CSS', 'Pollinations API', 'Stable Diffusion', 'Hugging Face'],
    gitURL: '',
    liveURL: '',
  },
  {
    id: 7,
    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=800&q=80',
    title: 'Pipeline Data & Dashboard Analytique',
    category: 'Projet Data Science',
    year: '2026',
    context: 'Analyse de données · Python · Pandas · Scikit-learn',
    description: 'Pipeline complet de traitement de données : exploration, nettoyage, transformation et visualisation interactive des indicateurs. Analyse exploratoire approfondie (EDA), modélisation statistique et comparaison de modèles de régression/classification. Focus sur la qualité du code, la reproductibilité et la lisibilité des résultats via un dashboard dynamique.',
    stack: ['Python', 'Pandas', 'NumPy', 'Scikit-learn', 'Matplotlib', 'Seaborn', 'Jupyter Notebook'],
    gitURL: '',
    liveURL: '',
  },
  {
    id: 8,
    image: 'https://images.unsplash.com/photo-1677442135703-1787eea5ce01?auto=format&fit=crop&w=800&q=80',
    title: 'Classification de Texte & Analyse de Sentiment (NLP) ( en cours)',
    category: 'Projet IA / NLP ( encours)',
    year: '2026',
    context: 'NLP · Python · TensorFlow · NLTK',
    description: 'Système NLP de classification automatique et d\'analyse de sentiment sur corpus textuel. Prétraitement linguistique complet (tokenisation, lemmatisation, vectorisation TF-IDF / word embeddings), entraînement et comparaison de modèles (Naive Bayes, SVM, LSTM), évaluation par métriques F1 / précision / rappel, et exposition via API REST Flask.',
    stack: ['Python', 'TensorFlow', 'NLTK', 'Scikit-learn', 'Pandas', 'Flask', 'Jupyter Notebook'],
    gitURL: '',
    liveURL: '',
  },
]);
</script>

<style scoped>
.screenshot-wrapper:hover .screenshot-overlay {
  opacity: 1;
}
.line-clamp-3 {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
</style>
