<template>
  <div class="layout">
    <Header />
    <main class="router-view">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';
</script>

<style lang="scss">
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;

  // router-view 區域要撐開剩下高度
  main,
  .router-view {
    flex: 1;
  }
}
</style>