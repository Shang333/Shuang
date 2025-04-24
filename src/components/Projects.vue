<template>
    <section id="projects" class="projects-section">
      <h2>Projects</h2>
      <div class="projects-grid">
        <ProjectCard
          v-for="(project, i) in projects"
          :key="i"
          :image="project.image"
          :title="project.title"
          :description="project.description"
          :techs="project.techs"
        />
      </div>
    </section>
  </template>
  
  <script setup>
  import ProjectCard from './ProjectCard.vue';
  
  const projects = [
    {
      title: 'Portfolio Website',
      image: '/images/project1.jpg',
      description: 'A personal portfolio site built with Vue 3 and SASS.',
      techs: ['Vue', 'SASS', 'HTML'],
    },
    {
      title: 'Blog API',
      image: '/images/project2.jpg',
      description: 'A backend API built with ASP.NET Core for managing blog posts.',
      techs: ['.NET Core', 'EF Core', 'SQL'],
    },
    {
      title: 'Portfolio Website',
      image: '/images/project1.jpg',
      description: 'A personal portfolio site built with Vue 3 and SASS.',
      techs: ['Vue', 'SASS', 'HTML'],
    },
    {
      title: 'Blog API',
      image: '/images/project2.jpg',
      description: 'A backend API built with ASP.NET Core for managing blog posts.',
      techs: ['.NET Core', 'EF Core', 'SQL'],
    },
    {
      title: 'Portfolio Website',
      image: '/images/project1.jpg',
      description: 'A personal portfolio site built with Vue 3 and SASS.',
      techs: ['Vue', 'SASS', 'HTML'],
    },
    {
      title: 'Blog API',
      image: '/images/project2.jpg',
      description: 'A backend API built with ASP.NET Core for managing blog posts.',
      techs: ['.NET Core', 'EF Core', 'SQL'],
    },
  ];
  </script>
  
  <style scoped lang="scss">
    .projects-section {
    padding: 3rem 2rem;
    max-width: 1200px;       // 限制整個區塊最大寬度
    margin: 0 auto;          // 置中

    h2 {
        text-align: center;
        margin-bottom: 2rem;
    }

    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); // 最多一行 4 張
        gap: 2rem;
        justify-content: center; // 卡片居中
    }
    }
  </style>
  