<template>
  <section class="hero">
    <div class="content">
      <h3 class="hello">
        <i class="pi pi-code"></i>
        Bonjour,
      </h3>

      <h1 class="title">
        Je suis
        <a
          href="https://www.linkedin.com/in/sarah-ferron-060658299/"
          target="_blank"
          class="name"
        >
          Sarah FERRON
        </a>
        <br />
        Etudiante ingénieure en informatique
      </h1>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.hero {
  padding: 6rem 4rem 6rem;
}

.content {
  width: 90%;
  max-width: 900px;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.hello {
  background: #f2f2f2;
  color: #555;
  padding: 0.4rem 0.8rem;
  border-radius: 8px;
  font-weight: 600;
  width: fit-content;
}

.title {
  font-size: clamp(1.8rem, 4vw, 3rem);
  font-weight: 700;
  line-height: 1.15;
  color: #444;
}

.name {
  color: #000;
  text-decoration: none;
}

.name:hover {
  text-decoration: underline;
}

.actions {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}

/* Responsive */
@media (max-width: 768px) {
  .hero {
    padding: 2rem 1.5rem;
  }

  .title {
    font-size: 2rem;
  }

  .actions {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>
