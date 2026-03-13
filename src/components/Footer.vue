<template>
  <footer class="bg-white border-t border-gray-100">
    <div class="max-w-screen-xl mx-auto px-6 md:px-12 lg:px-16 py-12">

      <div class="flex flex-col md:flex-row items-center justify-between gap-8">

        <!-- Identité -->
        <div class="text-center md:text-left">
          <div class="flex items-center gap-2.5 justify-center md:justify-start mb-2">
            <div class="w-8 h-8 rounded-lg bg-primary flex items-center justify-center">
              <span class="text-white font-bold text-sm leading-none">CT</span>
            </div>
            <span class="font-bold text-gray-900 text-base">Chelfy TABE</span>
          </div>
          <p class="text-gray-400 text-xs">Étudiant en L3 Informatique · Université Marie &amp; Louis Pasteur</p>
          <p class="text-gray-400 text-xs mt-0.5">Ingénierie Logicielle · Data & IA</p>
        </div>

        <!-- Navigation rapide -->
        <nav class="flex items-center gap-5 text-xs font-medium text-gray-400">
          <a href="#profil" class="hover:text-primary transition-colors">Profil</a>
          <a href="#formation" class="hover:text-primary transition-colors">Formation</a>
          <a href="#experiences" class="hover:text-primary transition-colors">Expériences</a>
          <a href="#competences" class="hover:text-primary transition-colors">Compétences</a>
          <a href="#projects" class="hover:text-primary transition-colors">Projets</a>
        </nav>

        <!-- Liens sociaux -->
        <div class="flex items-center gap-4">
          <a
            href="https://github.com/chelfy69"
            target="_blank"
            rel="noopener noreferrer"
            class="w-9 h-9 rounded-lg border border-gray-200 flex items-center justify-center text-gray-400 hover:text-primary hover:border-primary/30 transition-all"
            aria-label="GitHub"
          >
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
            </svg>
          </a>
          <a
            href="https://gitlab.com/Chelfy22"
            target="_blank"
            rel="noopener noreferrer"
            class="w-9 h-9 rounded-lg border border-gray-200 flex items-center justify-center text-gray-400 hover:text-primary hover:border-primary/30 transition-all"
            aria-label="GitLab"
          >
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M22.65 14.39L12 22.13 1.35 14.39a.84.84 0 01-.3-.94l1.22-3.78 2.44-7.51A.42.42 0 014.82 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.49h8.1l2.44-7.51A.42.42 0 0118.6 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.51L23 13.45a.84.84 0 01-.35.94z"/>
            </svg>
          </a>
          <a
            href="https://www.linkedin.com/in/chelfy-tabe-392783382"
            target="_blank"
            rel="noopener noreferrer"
            class="w-9 h-9 rounded-lg border border-gray-200 flex items-center justify-center text-gray-400 hover:text-primary hover:border-primary/30 transition-all"
            aria-label="LinkedIn"
          >
            <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
          </a>
        </div>

      </div>

      <!-- Bas de footer -->
      <div class="mt-10 pt-6 border-t border-gray-50 flex flex-col sm:flex-row items-center justify-between gap-3">
        <p class="text-xs text-gray-400">© 2026 Chelfy TABE. Tous droits réservés.</p>
        <p class="text-xs text-gray-400">Développé avec Vue.js 3 · Tailwind CSS · Vite</p>
      </div>

    </div>
  </footer>
</template>
