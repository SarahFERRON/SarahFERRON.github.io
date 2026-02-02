<template>
  <article :class="['card', { featured }]">
    <img :src="image" :alt="title" class="image" />

    <div class="content">
      <h4>{{ title }}</h4>
      <p>{{ description }}</p>
      <v-btn variant="text" size="small">
        <i class="pi pi-github"></i>
        Voir le projet →
      </v-btn>
    </div>
  </article>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  featured: Boolean,
})
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  height: 100%;
  background: white;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 10px 28px rgba(0, 0, 0, 0.08);
}

/* 🔥 même hauteur que les autres */
.image {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.content {
  padding: 1.4rem 1.6rem;
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
}

/* Featured = juste plus large, pas plus haut */
.card.featured {
  grid-column: span 2;
}

@media (max-width: 900px) {
  .card.featured {
    grid-column: span 1;
  }
}
</style>
