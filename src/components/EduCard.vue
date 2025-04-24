<template>
    <div class="edu-card">
      <h3>{{ title }}</h3>
      <h4 class="subtitle">{{ subtitle }}</h4>
      <p class="date">{{ date }}</p>
      <p class="description">{{ description }}</p>
    </div>
  </template>
  
  <script setup>
  defineProps(['title', 'subtitle', 'date', 'description']);
  </script>
  
  <style scoped lang="scss">
  .edu-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1.2rem;
    transition: box-shadow 0.3s ease;
    background: #fff;
  
    &:hover {
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.1);
    }
  
    h3 {
      font-size: 1.1rem;
      font-weight: bold;
      margin-bottom: 0.3rem;
    }
  
    .subtitle {
      font-size: 0.95rem;
      color: #666;
      margin-bottom: 0.5rem;
    }
  
    .date {
      font-size: 0.85rem;
      color: #aaa;
      margin-bottom: 0.8rem;
    }
  
    .description {
      font-size: 0.95rem;
      color: #333;
    }
  }
  </style>
  