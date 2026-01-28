<script setup>
import { ref } from 'vue'

const showMenu = ref(false)
</script>

<template>
  <nav class="navbar">
    <!-- Desktop -->
    <ul class="links">
      <li><a href="#">Home</a></li>
      <li><a href="#work">Works</a></li>
      <li><a href="#testimonial">Testimonials</a></li>
      <li><a href="#about">About</a></li>
    </ul>

    <!-- Burger -->
    <button class="burger" @click="showMenu = true">
      <span />
      <span />
      <span />
    </button>

    <!-- Mobile menu -->
    <div class="mobile-menu" :class="{ open: showMenu }">
      <button class="close" @click="showMenu = false">✕</button>
      <a href="#" @click="showMenu = false">Home</a>
      <a href="#work" @click="showMenu = false">Works</a>
      <a href="#testimonial" @click="showMenu = false">Testimonials</a>
      <a href="#about" @click="showMenu = false">About</a>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  width: 100%;
  padding: 1.2rem 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
}

.logo {
  font-weight: 600;
  font-size: 1.2rem;
}

.links {
  display: flex;
  gap: 2rem;
  list-style: none;
}

.links a {
  text-decoration: none;
  color: #403930;
  font-weight: 500;
  position: relative;
}

.links a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -4px;
  width: 0;
  height: 2px;
  background: #403930;
  transition: 0.25s ease;
}

.links a:hover::after {
  width: 100%;
}

/* Burger */
.burger {
  display: none;
  flex-direction: column;
  gap: 6px;
  background: none;
  border: none;
  cursor: pointer;
}

.burger span {
  width: 24px;
  height: 2px;
  background: #403930;
  border-radius: 2px;
}

/* Mobile menu */
.mobile-menu {
  position: fixed;
  inset: 0;
  background: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  font-size: 1.5rem;
  transform: translateY(-100%);
  transition: transform 0.35s ease;
  z-index: 100;
}

.mobile-menu.open {
  transform: translateY(0);
}

.mobile-menu a {
  text-decoration: none;
  color: #403930;
}

.close {
  position: absolute;
  top: 1.5rem;
  right: 2rem;
  background: none;
  border: none;
  font-size: 2rem;
  cursor: pointer;
}

/* Responsive */
@media (max-width: 768px) {
  .links {
    display: none;
  }

  .burger {
    display: flex;
  }
}
</style>
