<template>
  <header class="w-full z-50 sticky top-0 bg-white/90 backdrop-blur-md border-b border-gray-100">
    <nav class="max-w-screen-xl mx-auto flex items-center justify-between px-6 md:px-10 h-16">

      <!-- Logo -->
      <a href="#" class="flex items-center gap-2.5 group">
        <div class="w-8 h-8 rounded-lg bg-primary flex items-center justify-center flex-shrink-0">
          <span class="text-white font-bold text-sm leading-none">CT</span>
        </div>
        <span class="font-semibold text-gray-800 text-sm hidden sm:block tracking-tight">Chelfy TABE</span>
      </a>

      <!-- Desktop menu -->
      <ul class="hidden md:flex items-center gap-7 text-sm font-medium text-gray-500">
        <li v-for="item in Menu" :key="item.name">
          <a
            :href="item.href"
            class="hover:text-primary transition-colors duration-200 relative group"
            @click.prevent="scrollToSection(item.href)"
          >
            {{ item.name }}
            <span class="absolute -bottom-0.5 left-0 w-0 h-0.5 bg-primary rounded-full transition-all duration-300 group-hover:w-full"></span>
          </a>
        </li>
      </ul>

      <!-- CTA desktop -->
      <a
        href="#contact"
        @click.prevent="scrollToSection('#contact')"
        class="hidden md:inline-flex items-center gap-2 text-sm font-medium text-primary border border-primary/30 px-4 py-2 rounded-lg hover:bg-primary hover:text-white hover:border-primary transition-all duration-200"
      >
        Me contacter
      </a>

      <!-- Mobile toggle -->
      <button class="md:hidden p-2 rounded-lg hover:bg-gray-50 transition-colors" @click="isMenuOpen = !isMenuOpen">
        <svg v-if="!isMenuOpen" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/>
        </svg>
        <svg v-else width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/>
        </svg>
      </button>
    </nav>

    <!-- Mobile menu -->
    <div v-if="isMenuOpen" class="md:hidden border-t border-gray-100 bg-white px-6 py-4 space-y-1">
      <a
        v-for="item in Menu"
        :key="item.name"
        :href="item.href"
        class="block py-2.5 text-sm font-medium text-gray-600 hover:text-primary transition-colors"
        @click.prevent="scrollToSection(item.href)"
      >
        {{ item.name }}
      </a>
      <a
        href="#contact"
        class="block mt-3 text-center py-2.5 text-sm font-medium text-white bg-primary rounded-lg"
        @click.prevent="scrollToSection('#contact')"
      >
        Me contacter
      </a>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";
const isMenuOpen = ref(false);
const Menu = ref([
  { name: 'Profil',       href: '#profil' },
  { name: 'Formation',    href: '#formation' },
  { name: 'Expériences',  href: '#experiences' },
  { name: 'Compétences',  href: '#competences' },
  { name: 'Projets',      href: '#projects' },
  { name: 'Contact',      href: '#contact' },
]);

const scrollToSection = (href) => {
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>
