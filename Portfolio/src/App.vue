<template>
  <v-app>
    <Navbar />
    <v-main class="main">
      <Hero />
      <ProjectSection />
    </v-main>
  </v-app>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import ProjectSection from './components/ProjectSection.vue';
</script>

<style scoped>
.main {
  padding: 0 !important;
  min-height: auto !important;
}
</style>
