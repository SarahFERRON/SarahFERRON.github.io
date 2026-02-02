<template>
  <section id="work" class="work-section">
    <h3 class="heading">Mes projets</h3>

    <div class="cards">
      <ProjetCard
        title="Portfolio - Janvier 2026"
        description="Designed some empty state screens in kawaii style for the popular sheepify app. Tailwind lets you conditionally apply utility classes in different states using variant modifiers."
        image="/src/assets/project1.png"
      />
      <ProjetCard
        title="Building Devis - Septembre 2024 à Juin 2025"
        description="Designed some empty state screens in kawaii style for the popular sheepify app. Tailwind lets you conditionally apply utility classes in different states using variant modifiers."
        image="/src/assets/building-devis.png"
      />
      <ProjetCard
        title="Communes Bretonnes - Janvier 2024 à Juin 2024 "
        description="Designed some empty state screens in kawaii style for the popular sheepify app. Tailwind lets you conditionally apply utility classes in different states using variant modifiers."
        image="/src/assets/communes-bretonnes.png"
      />
      <ProjetCard
        title="Sporttrack V2 - Octobre 2024"
        description="Réalisation d'un site web de suivi de sport. En Octobre 2023, codage des pages (HTML/CSS), puis en Octobre 2024, création du site web en PHP puis en JavaScript en réutilisant les pages précédemment réalisées."
        image="/src/assets/sporttrack.png"
      />
      <ProjetCard
        title="Jeu de Wythoff - Novembre 2023"
        description="Designed some empty state screens in kawaii style for the popular sheepify app. Tailwind lets you conditionally apply utility classes in different states using variant modifiers."
        image="/src/assets/jeu-de-wythoff.png"
      />
    </div>
  </section>
</template>

<script setup>
import ProjetCard from './ProjectCard.vue'
</script>

<style scoped>
.work-section {
  padding: 5rem 3rem;
  display: flex;
  flex-direction: column;
  gap: 3rem;
  background-color: #ffddbf;
}

.heading {
  font-size: 2rem;
  font-weight: 700;
  color: #403930;
}

.cards {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}
</style>
