<template>
  <section class="relative w-full bg-white">
    <MainHero />
  </section>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
const MainHero = defineAsyncComponent(() => import('./MainHero.vue'));
</script>
