<template>
    <footer class="footer">
      <div class="container">
        <p>© {{ new Date().getFullYear() }} Sarah Ferron — Tous droits réservés</p>
  
        <div class="links">
          <a href="https://github.com/SarahFERRON" target="_blank">
            <i class="pi pi-github"></i>
            GitHub
          </a>
          <a href="https://www.linkedin.com/" target="_blank">
            <i class="pi pi-linkedin"></i>
            LinkedIn
          </a>
          <a href="mailto:sarah.ferron.2005@gmail.com">
            <i class="pi pi-envelope"></i>
            Contact
          </a>
        </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .footer {
    background: white;
    color: #403930;
    padding: 2rem 1.5rem;
    margin-top: 4rem;
  }
  
  .container {
    max-width: 1200px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 1rem;
    align-items: center;
  }
  
  .links {
    display: flex;
    gap: 1.5rem;
  }
  
  .links a {
    color: #403930;
    text-decoration: none;
    font-weight: 500;
    opacity: 0.85;
    transition: opacity 0.2s ease;
  }
  
  .links a:hover {
    opacity: 1;
    text-decoration: underline;
  }
  </style>
  