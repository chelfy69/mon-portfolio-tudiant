<template>
  <section class="py-10 bg-white border-y border-gray-100 overflow-hidden select-none">

    <!-- Label -->
    <p class="text-center text-xs font-medium text-gray-400 uppercase tracking-widest mb-7">
      Technologies &amp; outils maîtrisés
    </p>

    <!-- Première rangée — défilement gauche -->
    <div class="marquee-wrapper mb-4">
      <div class="marquee-track">
        <div
          v-for="(tech, i) in [...row1, ...row1]"
          :key="`r1-${i}`"
          class="tech-pill"
        >
          <img :src="tech.icon" :alt="tech.name" class="w-6 h-6 object-contain flex-shrink-0" />
          <span translate="no" class="text-xs font-medium text-gray-600 whitespace-nowrap">{{ tech.name }}</span>
        </div>
      </div>
    </div>

    <!-- Deuxième rangée — défilement droite (inverse) -->
    <div class="marquee-wrapper">
      <div class="marquee-track marquee-reverse">
        <div
          v-for="(tech, i) in [...row2, ...row2]"
          :key="`r2-${i}`"
          class="tech-pill"
        >
          <img :src="tech.icon" :alt="tech.name" class="w-6 h-6 object-contain flex-shrink-0" />
          <span translate="no" class="text-xs font-medium text-gray-600 whitespace-nowrap">{{ tech.name }}</span>
        </div>
      </div>
    </div>

  </section>
</template>

<script setup>
import { ref } from 'vue';

const row1 = ref([
  { name: 'Vue.js',        icon: 'https://img.icons8.com/fluency/48/vuejs.png' },
  { name: 'Nuxt.js',       icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg' },
  { name: 'React',         icon: 'https://img.icons8.com/plasticine/100/react.png' },
  { name: 'Tailwind CSS',  icon: 'https://img.icons8.com/color/48/tailwindcss.png' },
  { name: 'JavaScript',    icon: 'https://img.icons8.com/color/48/javascript--v1.png' },
  { name: 'TypeScript',    icon: 'https://img.icons8.com/fluency/48/typescript--v2.png' },
  { name: 'HTML5',         icon: 'https://img.icons8.com/fluency/48/html-5.png' },
  { name: 'CSS3',          icon: 'https://img.icons8.com/fluency/48/css3.png' },
  { name: 'Figma',         icon: 'https://img.icons8.com/fluency/48/figma.png' },
  { name: 'Flutter',       icon: 'https://img.icons8.com/fluency/48/flutter.png' },
]);

const row2 = ref([
  { name: 'Node.js',       icon: 'https://img.icons8.com/fluency/48/node-js.png' },
  { name: 'Python',        icon: 'https://img.icons8.com/color/48/python.png' },
  { name: 'Symfony',       icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/symfony/symfony-original.svg' },
  { name: 'PHP',           icon: 'https://img.icons8.com/officel/48/php-logo.png' },
  { name: 'MySQL',         icon: 'https://img.icons8.com/fluency/48/mysql-logo.png' },
  { name: 'PostgreSQL',    icon: 'https://img.icons8.com/color/48/postgreesql.png' },
  { name: 'MongoDB',       icon: 'https://img.icons8.com/color/48/mongodb.png' },
  { name: 'TensorFlow',    icon: 'https://img.icons8.com/color/48/tensorflow.png' },
  { name: 'Git',           icon: 'https://img.icons8.com/color/48/git.png' },
  { name: 'Docker',        icon: 'https://img.icons8.com/fluency/48/docker.png' },
]);
</script>

<style scoped>
.marquee-wrapper {
  display: flex;
  overflow: hidden;
  -webkit-mask-image: linear-gradient(
    to right,
    transparent 0%,
    black 12%,
    black 88%,
    transparent 100%
  );
  mask-image: linear-gradient(
    to right,
    transparent 0%,
    black 12%,
    black 88%,
    transparent 100%
  );
}

.marquee-track {
  display: flex;
  align-items: center;
  gap: 10px;
  width: max-content;
  animation: marquee-left 35s linear infinite;
}

.marquee-reverse {
  animation: marquee-right 38s linear infinite;
}

.tech-pill {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 7px 14px;
  border-radius: 100px;
  border: 1px solid #e5e7eb;
  background: #f9fafb;
  flex-shrink: 0;
  transition: border-color 0.2s, background 0.2s;
}

.tech-pill:hover {
  border-color: rgba(12, 167, 255, 0.3);
  background: rgba(12, 167, 255, 0.04);
}

@keyframes marquee-left {
  0%   { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

@keyframes marquee-right {
  0%   { transform: translateX(-50%); }
  100% { transform: translateX(0); }
}

/* Pause on hover */
.marquee-wrapper:hover .marquee-track {
  animation-play-state: paused;
}
</style>
