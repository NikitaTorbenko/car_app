<script setup>
import { ref } from 'vue';
import MyInput from './UI/MyInput.vue';
import Zoom from '../assets/icons/zoom.svg';
import MyButton from './UI/MyButton.vue';
import Plus from '../assets/icons/white_plus.svg';
import { perPage } from '../consts';

const searchInputValue = ref('');
</script>

<template>
  <div class="main-top">
    <div class="main-top-inner">
      <MyInput
        v-model="searchInputValue"
        class-name="input"
        :icon="Zoom"
        placeholder="Search VIN"
      />
      <div class="select-block">
        <div class="select-block-text">Select vehicles per page:</div>
        <div class="select-block-inner">
          {{ perPage }}
          <img src="../assets/icons/chevron.svg" alt="" />
        </div>
      </div>
    </div>
    <MyButton text="Add Vechicle" :icon="Plus" class-name="button" />
  </div>
</template>

<style scoped lang="scss">
.main-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 32px;

  &-inner {
    display: flex;
    align-items: center;
    gap: 32px;

    @media (max-width: 1200px) {
      flex-direction: column;
    }
  }

  @media (max-width: 880px) {
    flex-direction: column;
  }
}

.input {
  max-width: 354px;
  width: 100%;
}

.button {
  color: #fff;
  background-color: #d90e32;
  @media (max-width: 880px) {
    margin-top: 32px;
  }
}

.select-block {
  display: flex;
  align-items: center;
  &-text {
    font-size: 16px;
    font-weight: 400;
    margin-right: 16px;
  }

  &-inner {
    padding: 9px 16px;
    border-radius: 8px;
    border: 1px solid #e4e4e4;
    display: flex;
    align-items: center;
    gap: 15px;
  }
}
</style>
