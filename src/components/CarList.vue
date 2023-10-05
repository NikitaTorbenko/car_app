<script setup>
import Car from './Car.vue';
import { cars } from '../consts';
</script>

<template>
  <div class="car-list">
    <Car
      v-for="car in cars"
      :key="car.name"
      :total="car.total"
      :selected="car.selected"
      :car-name="car.name"
      :car-number="car.number"
      :date="car.date"
      car-img="src/assets/img/mersedes.png"
    />
  </div>
</template>

<style scoped lang="scss">
.car-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(354px, 1fr));
  justify-items: center;
  gap: 30px;

  @media (max-width: 425px) {
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  }
}
</style>
