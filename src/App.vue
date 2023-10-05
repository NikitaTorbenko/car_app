<script setup>
import Header from './components/Header.vue';
import Sidebar from './components/Sidebar.vue';
import MainPage from './components/MainPage.vue';
</script>

<template>
  <div class="root">
    <Sidebar />
    <Header />
    <MainPage />
  </div>
</template>

<style lang="scss">
.root {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 256px 1fr;
  grid-template-rows: auto 1fr;
  grid-template-areas:
    'sidebar header'
    'sidebar main';

  @media (max-width: 680px) {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      'sidebar'
      'header'
      'main';
  }
}
</style>
