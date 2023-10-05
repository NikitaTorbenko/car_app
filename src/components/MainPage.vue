<script setup>
import MainTop from './MainTop.vue';
import Footer from './Footer.vue';
import CarList from './CarList.vue';
</script>

<template>
  <div class="main">
    <MainTop />
    <CarList />
    <Footer />
  </div>
</template>

<style scoped lang="scss">
.main {
  height: fit-content;
  grid-area: main;
  padding: 32px 30px 0;

  @media (max-width: 425px) {
    padding: 20px 12px 0;
  }
}
</style>
