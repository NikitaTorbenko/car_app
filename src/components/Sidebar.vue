<script setup>
import { ref } from 'vue';
import { listItemsForSidebar } from '../consts';
const activeItem = ref(1);
</script>

<template>
  <div class="sidebar">
    <h2 class="title">Demo Test</h2>
    <ul class="list">
      <li
        v-for="(item, index) in listItemsForSidebar"
        :key="item.id"
        :class="
          index === activeItem ? 'list-item list-item-active' : 'list-item'
        "
      >
        <div class="list-item-icon-wrap">
          <img class="list-item-icon" :src="item.icon" alt="" />
        </div>
        <span class="list-item-title">{{ item.title }}</span>
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.sidebar {
  grid-area: sidebar;
  background-color: #282828;
  color: #fff;
  height: 100%;
  width: 256px;
}

.title {
  font-size: 24px;
  font-weight: 700;
  text-align: center;
  margin-top: 30px;
}

.list {
  margin-top: 100px;
}

.list-item {
  cursor: pointer;
  display: flex;
  align-items: center;
  margin-bottom: 16px;
  padding: 12px 30px;
  transition: 0.2s;
  border-left: 2px solid #d90e3200;

  &:last-child {
    margin-bottom: 0;
  }

  &-active,
  &:hover {
    border-left: 2px solid #d90e32;

    background-color: rgba(255, 255, 255, 0.2);
    & .list-item-title {
      opacity: 1;
    }
  }

  &-icon-wrap {
    margin-right: 20px;
  }

  &-title {
    opacity: 0.45;
  }
}
</style>
