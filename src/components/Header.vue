<template>
  <header class="site-header">
    <div class="container">
      <h1 class="logo">Shuang</h1>
      <nav>
        <ul>
          <li><router-link to="/">About</router-link></li>
          <li><router-link to="/projects">Projects</router-link></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use '@/assets/styles/_variables' as *;

.site-header {
  background-color: #2d2d2d;
  color: white;
  padding: 1rem 2rem;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    font-size: 1.5rem;
    font-weight: bold;
  }

  nav ul {
    display: flex;
    gap: 1rem;
    list-style: none;

    a {
      color: white;
      text-decoration: none;
      &.router-link-exact-active {
        border-bottom: 2px solid $accent-color;
      }
      &:hover {
        text-decoration: underline;
      }
    }
  }
}
</style>