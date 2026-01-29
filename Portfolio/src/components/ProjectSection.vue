<template>
  <section id="work" class="work-section">
    <h3 class="heading">Mes projets</h3>

    <div class="cards">
      <ProjetCard
        title="Sheepify States"
        description="Designed some empty state screens in kawaii style for the popular sheepify app. Tailwind lets you conditionally apply utility classes in different states using variant modifiers."
        image="/src/assets/project1.png"
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
  background-color: #ffeed9;
}

.heading {
  font-size: 2rem;
  font-weight: 700;
  color: #333;
}

.cards {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}
</style>
