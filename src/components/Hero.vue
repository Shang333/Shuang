<template>
    <section class="hero">
      <img class="avatar" src="/images/avatar.jpg" alt="My Photo" />
      <h1>李雙</h1>
      <p>.Net C# 後端工程師</p>
      <div class="skills">
        <span>C#</span>
        <span>.NET Core</span>
        <span>MS SQL</span>
        <span>Git</span>
      </div>
    </section>
  </template>
  
  <style scoped lang="scss">
  .hero {
    padding: 60px 20px;
    text-align: center;
    .avatar {
      width: 120px;
      border-radius: 50%;
      margin-bottom: 20px;
    }
    .skills {
      margin-top: 10px;
      span {
        background: #eee;
        padding: 5px 10px;
        margin: 0 5px;
        border-radius: 5px;
        font-size: 14px;
      }
    }
  }
  </style>
  