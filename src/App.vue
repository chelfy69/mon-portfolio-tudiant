<template>
  <div class="min-h-screen bg-white">
    <Suspense>
      <template #default>
        <div>
          <NavBar />
          <HeroSection />
          <TechBand />
          <Services />
          <Education />
          <Experience />
          <Skills />
          <Projects />
          <ContactMe />
          <Footer />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';
AOS.init({ duration: 800, delay: 100, once: true });

import LoadingSpinner from './components/LoadingSpinner.vue';
const NavBar      = defineAsyncComponent(() => import('./components/NavBar.vue'));
const HeroSection = defineAsyncComponent(() => import('./components/HeroSection.vue'));
const TechBand    = defineAsyncComponent(() => import('./components/TechBand.vue'));
const Services    = defineAsyncComponent(() => import('./components/Services.vue'));
const Education   = defineAsyncComponent(() => import('./components/Education.vue'));
const Experience  = defineAsyncComponent(() => import('./components/Experience.vue'));
const Skills      = defineAsyncComponent(() => import('./components/Skills.vue'));
const Projects    = defineAsyncComponent(() => import('./components/Projects.vue'));
const ContactMe   = defineAsyncComponent(() => import('./components/ContactMe.vue'));
const Footer      = defineAsyncComponent(() => import('./components/Footer.vue'));
const BackToTop   = defineAsyncComponent(() => import('./components/BackToTop.vue'));
</script>
