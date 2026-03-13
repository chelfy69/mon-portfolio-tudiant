<template>
  <div class="w-full px-6 sm:px-10 md:px-12 lg:px-16 max-w-screen-xl mx-auto">
    <div class="grid lg:grid-cols-2 gap-12 xl:gap-16 items-center min-h-[88vh] py-16">

      <!-- Texte gauche -->
      <div data-aos="fade-up" class="flex flex-col gap-6 text-center lg:text-left">

        <!-- Badge statut -->
        <div class="flex justify-center lg:justify-start">
          <span class="inline-flex items-center gap-2 text-xs font-medium text-primary bg-primary/8 border border-primary/20 px-3.5 py-1.5 rounded-full">
            <span class="w-1.5 h-1.5 rounded-full bg-green-400 animate-pulse"></span>
            Étudiant ambitieux · Développement & Ingénierie Logicielle
          </span>
        </div>

        <!-- Identité -->
        <div>
          <p class="text-sm font-medium text-gray-400 uppercase tracking-widest mb-2">Bonjour, je suis</p>
          <h1 class="font-bold text-4xl md:text-5xl text-gray-900 leading-tight tracking-tight">
            Chelfy TABE
          </h1>
          <p class="text-primary font-medium text-lg mt-2">Développeur Full-Stack</p>
        </div>

        <!-- Bio courte -->
        <p class="text-gray-500 text-[15px] leading-relaxed max-w-lg mx-auto lg:mx-0">
          Étudiant en Licence 3 Informatique à l'Université Marie &amp; Louis Pasteur (Montbéliard),
          je m'oriente vers l'ingénierie logicielle avec un intérêt marqué pour la conception
          de systèmes robustes, la structuration du code et l'intégration de briques data/IA.
        </p>

        <!-- Actions -->
        <div class="flex flex-col sm:flex-row items-center gap-3 justify-center lg:justify-start">
          <!-- Contact -->
          <a
            href="#contact"
            class="w-full sm:w-auto flex items-center justify-center gap-2 bg-primary text-white font-medium text-sm px-6 py-3 rounded-xl hover:bg-primary/90 transition-all hover:-translate-y-0.5 hover:shadow-md"
          >
            Me contacter
          </a>

          <!-- CV download -->
          <a
            href="/CV_.pdf"
            download="CV_Chelfy_TABE.pdf"
            class="w-full sm:w-auto flex items-center justify-center gap-3 px-5 py-3 rounded-xl border border-gray-200 bg-white hover:border-primary/40 hover:shadow-md hover:-translate-y-0.5 transition-all group"
          >
            <div class="w-8 h-8 rounded-lg bg-primary/10 flex items-center justify-center group-hover:bg-primary/20 transition-colors">
              <svg width="15" height="15" viewBox="0 0 18 22" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M13 9L9 13M9 13L5 9M9 13V1" stroke="#0CA7ff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M1 17V18C1 19.657 2.343 21 4 21H14C15.657 21 17 19.657 17 18V17" stroke="#0CA7ff" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>
            <div class="text-left">
              <p class="text-[11px] text-gray-400 leading-none">Curriculum Vitae</p>
              <p class="text-sm font-semibold text-gray-700 leading-tight mt-0.5">Télécharger</p>
            </div>
            <span class="text-[10px] font-bold text-white bg-primary px-2 py-0.5 rounded-full">PDF</span>
          </a>
        </div>

        <!-- Liens sociaux -->
        <div class="flex items-center gap-4 justify-center lg:justify-start pt-1">
          <a href="https://github.com/chelfy69" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-gray-700 transition-colors text-xs flex items-center gap-1.5">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
            </svg>
            GitHub
          </a>
          <span class="text-gray-200">·</span>
          <a href="https://gitlab.com/Chelfy22" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-gray-700 transition-colors text-xs flex items-center gap-1.5">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M22.65 14.39L12 22.13 1.35 14.39a.84.84 0 01-.3-.94l1.22-3.78 2.44-7.51A.42.42 0 014.82 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.49h8.1l2.44-7.51A.42.42 0 0118.6 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.51L23 13.45a.84.84 0 01-.35.94z"/>
            </svg>
            GitLab
          </a>
          <span class="text-gray-200">·</span>
          <a href="https://www.linkedin.com/in/chelfy-tabe-392783382" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-primary transition-colors text-xs flex items-center gap-1.5">
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
            LinkedIn
          </a>
        </div>
      </div>

      <!-- Photo droite -->
      <div data-aos="fade-up" data-aos-delay="150" class="flex justify-center items-center">
        <div class="relative flex flex-col items-center gap-6">

          <!-- Lueur -->
          <div class="absolute w-64 h-64 rounded-full bg-primary/10 blur-3xl top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 pointer-events-none"></div>

          <!-- Points décoratifs -->
          <div class="absolute top-4 right-8 w-2.5 h-2.5 rounded-full bg-primary/40 z-20"></div>
          <div class="absolute top-12 right-2 w-1.5 h-1.5 rounded-full bg-primary/20 z-20"></div>
          <div class="absolute bottom-20 left-4 w-2.5 h-2.5 rounded-full bg-primary/35 z-20"></div>
          <div class="absolute bottom-12 left-10 w-1.5 h-1.5 rounded-full bg-primary/15 z-20"></div>

          <!-- Hexagone -->
          <div class="hexagon-container">
            <div class="hexagon-outer">
              <div class="hexagon-inner">
                <img src="../../21.jpg" alt="Chelfy TABE" class="w-full h-full object-cover" style="object-position: center 12%;"/>
              </div>
            </div>
          </div>

          <!-- Badge -->
          <div class="relative z-20">
            <div class="flex items-center gap-2 rounded-full border border-primary/20 bg-white py-2.5 px-5 shadow-sm">
              <span class="w-2 h-2 rounded-full bg-green-400 animate-pulse flex-shrink-0"></span>
              <span class="text-sm font-medium text-gray-700">L3 Informatique · Montbéliard</span>
            </div>
          </div>

        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
const NavBar = defineAsyncComponent(() => import('./NavBar.vue'));
</script>

<style scoped>
.hexagon-container {
  filter: drop-shadow(0 8px 28px rgba(12, 167, 255, 0.30));
  position: relative;
  z-index: 10;
}
.hexagon-outer {
  width: 270px;
  height: 305px;
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  background: linear-gradient(160deg, #0CA7ff 0%, #0060cc 60%, #003d99 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}
.hexagon-inner {
  width: 260px;
  height: 295px;
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  overflow: hidden;
  flex-shrink: 0;
}
.hexagon-inner img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 22%;
  transform: scale(1.0);
  transform-origin: center 22%;
}
</style>
