<template>
  <section id="contact" class="bg-gray-50 py-24 px-6 md:px-12 lg:px-16">
    <div class="max-w-screen-xl mx-auto">

      <!-- En-tête -->
      <div class="mb-16 text-center" data-aos="fade-up">
        <p class="text-xs font-semibold text-primary uppercase tracking-widest mb-3">Contact</p>
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 leading-tight">
          Échangeons
        </h2>
        <p class="text-gray-500 text-sm mt-3 max-w-md mx-auto">
          Disponible pour tout échange académique, opportunité de stage ou collaboration technique.
        </p>
      </div>

      <div class="max-w-lg mx-auto space-y-4" data-aos="fade-up">

        <!-- Informations de contact -->
        <div
          v-for="item in contactInfo"
          :key="item.id"
          class="flex items-center gap-4 p-5 bg-white rounded-2xl border border-gray-100 hover:border-primary/20 hover:shadow-sm transition-all"
        >
          <div class="w-10 h-10 rounded-xl bg-primary/10 flex items-center justify-center flex-shrink-0">
            <span v-html="item.icon" class="text-primary"></span>
          </div>
          <div>
            <p class="text-xs text-gray-400 mb-0.5">{{ item.label }}</p>
            <a
              v-if="item.href"
              :href="item.href"
              target="_blank"
              rel="noopener noreferrer"
              class="text-sm font-medium text-gray-700 hover:text-primary transition-colors"
            >{{ item.value }}</a>
            <p v-else class="text-sm font-medium text-gray-700">{{ item.value }}</p>
          </div>
        </div>

        <!-- Liens sociaux -->
        <div class="p-5 bg-white rounded-2xl border border-gray-100">
          <p class="text-xs text-gray-400 mb-4">Retrouvez-moi également sur</p>
          <div class="flex items-center gap-5">
            <a
              v-for="social in socials"
              :key="social.name"
              :href="social.href"
              target="_blank"
              rel="noopener noreferrer"
              class="flex items-center gap-2 text-sm font-medium text-gray-500 hover:text-primary transition-colors group"
            >
              <span v-html="social.icon" class="group-hover:text-primary transition-colors"></span>
              {{ social.name }}
            </a>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const contactInfo = ref([
  {
    id: 1,
    label: 'Adresse e-mail',
    value: 'chelfytabe69@mail.com',
    href: 'mailto:chelfytabe69@mail.com',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>`,
  },
  {
    id: 2,
    label: 'Téléphone',
    value: '07 43 52 08 25',
    href: 'tel:+33743520825',
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.09 9.81a19.79 19.79 0 01-3.07-8.67A2 2 0 012 0h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L6.09 7.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z"/></svg>`,
  },
  {
    id: 3,
    label: 'Localisation',
    value: 'Montbéliard, France',
    href: null,
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>`,
  },
]);

const socials = ref([
  {
    name: 'GitHub',
    href: 'https://github.com/chelfy69',
    icon: `<svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>`,
  },
  {
    name: 'GitLab',
    href: 'https://gitlab.com/Chelfy22',
    icon: `<svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M22.65 14.39L12 22.13 1.35 14.39a.84.84 0 01-.3-.94l1.22-3.78 2.44-7.51A.42.42 0 014.82 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.49h8.1l2.44-7.51A.42.42 0 0118.6 2a.43.43 0 01.58 0 .42.42 0 01.11.18l2.44 7.51L23 13.45a.84.84 0 01-.35.94z"/></svg>`,
  },
  {
    name: 'LinkedIn',
    href: 'https://www.linkedin.com/in/chelfy-tabe-392783382',
    icon: `<svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>`,
  },
]);
</script>
