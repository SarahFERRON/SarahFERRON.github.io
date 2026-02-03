<template>
  <nav class="navbar">
    <div class="logo">Portfolio</div>

    <!-- Desktop links -->
    <ul class="nav-links" :class="{ open: showMenu }">
      <li><a href="#">Accueil</a></li>
      <li><a href="#work">Projets</a></li>
      <li><a href="#testimonial">Testimonials</a></li>
      <li><a href="#about">About</a></li>
    </ul>

    <!-- Mobile toggle -->
    <button class="burger" @click="showMenu = !showMenu">
      <span></span>
      <span></span>
      <span></span>
    </button>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
const showMenu = ref(false)
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 2rem;
  background: #ffddbf;
  position: sticky;
  top: 0;
  z-index: 50;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
}

.logo {
  font-weight: bold;
  font-size: 1.5rem;
  color: #403930;
}

.nav-links {
  display: flex;
  gap: 3rem;
  list-style: none;
}

.nav-links li a {
  color: #403930;
  text-decoration: none;
  font-weight: 300;
  font-size: 1.4rem;
  transition: 0.3s;
}

.nav-links li a:hover {
  color: #00bfa5;
}

.burger {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 25px;
  height: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
}

.burger span {
  height: 3px;
  width: 100%;
  background: #403930;
  border-radius: 3px;
}

@media (max-width: 768px) {
  .burger {
    display: flex;
  }

  .nav-links {
    position: absolute;
    right: 0;
    top: 70px;
    flex-direction: column;
    background: #fff;
    width: 200px;
    padding: 1rem;
    gap: 1rem;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    transform: translateX(100%);
    transition: transform 0.3s ease-in-out;
  }

  .nav-links.open {
    transform: translateX(0);
  }
}
</style>
