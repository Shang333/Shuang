<template>
    <section id="projects" class="projects-section">
      <h2>Projects</h2>
      <div class="projects-grid">
        <ProjectCard
          v-for="(project, i) in projects"
          :key="i"
          :title="project.title"
          :description="project.description"
          :techs="project.techs"
          :github="project.github"
        />
      </div>
    </section>
  </template>
  
  <script setup>
  import ProjectCard from './ProjectCard.vue';
  
  const projects = [
    {
      title: '個人網站製作',
      description: '使用Vue 3 (Vite) 製作個人網站(也就是本網站)。',
      techs: ['Vue 3', 'CSS', 'HTML','Javascript'],
      github: 'https://github.com/Shang333/Shuang'
    },
    {
      title: 'SOLID原則實作',
      description: '以SOLID原則建構專案、撰寫程式，功能包含顯示doc、xlxs、pdf對應的文字，與上傳檔案。',
      techs: ['.NET Core 8', 'EF Core'],
      github: 'https://github.com/Shang333/SOLID_Practice1'
    },
    {
      title: '新聞爬蟲網站',
      description: '使用Python撰寫爬蟲，針對BBC、CNN的新聞爬取，並匯出成excel檔。',
      techs: ['.NET Core 8 MVC', 'EF Core', 'MSSQL', 'Python'],
      github: 'https://github.com/Shang333/FetchNewsProjocet'
    },
    {
      title: '專案模組化與單元測試',
      description: '以模組化的方式分類程式碼，並使用NUNIT撰寫單元測試。',
      techs: ['.NET Core 8', 'EF Core', 'SQL', 'Unit Test'],
      github: 'https://github.com/Shang333/APIModuleTest1'
    }
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
  