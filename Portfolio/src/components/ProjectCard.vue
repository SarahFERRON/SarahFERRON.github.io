<template>
  <article :class="['card', { featured }]">
    <img :src="image" :alt="title" class="image" />

    <div class="content">
      <h4 style="font-weight: bold;">{{ title }}</h4>
      <p>{{ description }}</p>
      <p class="tech">Technologies : {{ technologies }}</p>
      <v-btn 
        class="btn px-3"
        color="#403930" 
        size="small" 
        target="_blank"
        rel="noopener"
        :href="page"
      >
        <i class="pi pi-github"></i>
        Voir le projet
      </v-btn>
    </div>
  </article>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  technologies: String,
  image: String,
  featured: Boolean,
  page: String,
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

.btn {
  align-self: center;
  width: fit-content;
  padding-inline: 0;
}

.tech {
  font-weight: 600;
  color: #403930;
  margin-top: 0.3rem;
}

@media (max-width: 900px) {
  .card.featured {
    grid-column: span 1;
  }
}
</style>
