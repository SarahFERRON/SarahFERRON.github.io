<template>
    <article class="card">
      <div class="text">
        <h4 class="title">{{ title }}</h4>
        <p class="description">{{ description }}</p>
        <v-btn variant="text" color="primary" class="btn">
          View Case Study
        </v-btn>
      </div>
  
      <div class="image-wrapper">
        <img :src="image" alt="" />
      </div>
    </article>
  </template>
  
  <script setup>
  defineProps({
    title: String,
    description: String,
    image: String,
  })
  </script>
  
  <style scoped>
  .card {
    display: flex;
    gap: 3rem;
    background: #fff;
    border-radius: 24px;
    overflow: hidden;
    align-items: center;
  }
  
  .text {
    flex: 1;
    padding: 3rem;
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }
  
  .title {
    font-size: 1.6rem;
    font-weight: 700;
    color: #333;
  }
  
  .description {
    color: #555;
    line-height: 1.6;
  }
  
  .btn {
    align-self: flex-start;
    font-weight: 600;
  }
  
  /* Image */
  .image-wrapper {
    flex: 1;
    background: #e9f5ec;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .image-wrapper img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  
  /* Responsive */
  @media (max-width: 900px) {
    .card {
      flex-direction: column-reverse;
    }
  
    .text {
      padding: 2rem;
    }
  }
  </style>
  