<template>
  <section id="work" class="work-section">
    <h3 class="heading">Mes projets</h3>

    <div class="grid">
      <ProjetCard v-bind="projects[0]" featured />
      <ProjetCard
        v-for="(project, index) in projects.slice(1)"
        :key="index"
        v-bind="project"
      />
    </div>
  </section>
</template>


<script setup>
import ProjetCard from './ProjectCard.vue'

const projects = [
  {
    title: 'Portfolio - Janvier 2026',
    description:
      'Portfolio personnel en Vue 3 et Vuetify mettant en avant mes projets récents.',
    technologies: 'Vue 3, Vuetify',
    image: '/images/portfolio.png',
    page:'https://github.com/SarahFERRON/SarahFERRON.github.io',
  },
  {
    title: 'Building Devis - Septembre 2024 à Juin 2025',
    description:
      'Application web de gestion de rendez-vous avec des artisans. L\'appliction localise les artisans les plus près de vous et permet d\'échanger avec eux via une messagerie.',
    technologies: 'Vue 3, Ionic, PostgreSQL',
    image: '/images/building-devis.png',
    page:'https://github.com/SarahFERRON/building-devis',
  },
  {
    title: 'Communes Bretonnes - Janvier 2024 à Juin 2024',
    description:
      'Application de valorisation du patrimoine breton en présentant les facteurs d\'attractivité d\'une commune.',
    technologies: 'Java, JavaFX, MySQL',
    image: '/images/communes-bretonnes.png',
    page:'https://github.com/SarahFERRON/communes-bretonnes',
  },
  {
    title: 'Sporttrack V2 - Octobre 2024',
    description:
      'Application de suivi sportif avec historique et statistiques. Le projet a été réalisé dans un premier temps en Octobre 2023 avec le codage des pages HTML/CSS, puis dans un second temps en Octobre 2024 avec la création du site web en PHP puis en Javascript.',
    technologies: 'HTML, CSS, PHP, JavaScript',
    image: '/images/sporttrack.png',
    page:'https://github.com/SarahFERRON/sporttrack-v2-js',
  },
  {
    title: 'Jeu de Wythoff - Novembre 2023',
    description:
      'Jeu mathématique en Java avec une version de jeu humain contre humain et une seconde humain contre ordinateur avec une stratégie gagnante.',
    technologies: 'Java',
    image: '/images/jeu-de-wythoff.png',
    page:'https://github.com/SarahFERRON/wythoff-game',
  },
]
</script>

<style scoped>
.work-section {
  padding: 4rem 3rem;
  background-color: #ffddbf;
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

.heading {
  font-size: 2.2rem;
  font-weight: 700;
  color: #403930;
  text-align: left;
  max-width: 1200px;
}

/* Featured */
.featured {
  max-width: 100%;
}

/* Grid */
.grid {
  max-width: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2.5rem;
}

/* Responsive */
@media (max-width: 900px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
</style>
