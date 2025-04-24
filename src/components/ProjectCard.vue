<template>
    <div class="project-card">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <div class="tech-list">
        <span v-for="tech in techs" :key="tech">{{ tech }}</span>
      </div>
    </div>
  </template>
  
  <script setup>
  defineProps(['image', 'title', 'description', 'techs']);
  </script>
  
  <style scoped lang="scss">
  .project-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1rem;
    transition: box-shadow 0.3s;
    &:hover {
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
  
    .thumbnail {
      width: 100%;
      border-radius: 6px;
      object-fit: cover;
      margin-bottom: 0.5rem;
    }
  
    .tech-list {
      margin-top: 0.5rem;
      span {
        background: #eee;
        padding: 4px 8px;
        margin-right: 6px;
        border-radius: 4px;
        font-size: 12px;
      }
    }
  }
  </style>
  