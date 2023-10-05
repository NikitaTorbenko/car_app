<script setup>
defineProps({
  total: {
    type: Number,
    required: true,
  },
  selected: {
    type: Number,
    required: true,
  },
  carNumber: {
    type: String,
    required: true,
  },
  carName: {
    type: String,
    required: true,
  },
  date: {
    type: String,
    required: true,
  },
  carImg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="car">
    <div class="more_horizontal"></div>
    <img class="car-img" :src="carImg" alt="" />
    <h3 class="brand">{{ carName }}</h3>
    <div class="number">{{ carNumber }}</div>
    <div class="line"></div>
    <div class="info">
      <div :class="selected === total ? 'count count-green' : 'count'">
        <img v-if="selected === total" src="../assets/icons/check.svg" alt="" />
        {{ selected }}/{{ total }}
      </div>
      <div class="date">{{ date }}</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.car {
  height: fit-content;
  max-width: 354px;
  width: 100%;
  position: relative;
  border-radius: 10px;
  background-color: #f3f6f8;
  padding: 40px 24px 16px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.more_horizontal {
  position: absolute;
  width: 24px;
  height: 24px;
  cursor: pointer;
  top: 20px;
  right: 20px;
  background-image: url('../assets/img/more_horizontal.png');
}

.car-img {
  width: 260px;
  height: 135px;
  margin: 0 auto;
}

.brand {
  color: #293148;
  font-size: 20px;
  font-weight: 700;
  margin-top: 24px;
}

.number {
  color: rgba(41, 49, 72, 0.6);
  font-size: 15px;
  font-weight: 500;
  letter-spacing: 0.3px;
  margin-top: 12px;
}

.line {
  height: 1px;
  background-color: #e4e4e4;
  margin: 18px 0;
}

.info {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.count {
  border-radius: 6px;
  background-color: #ededed;
  padding: 4px 14px;
  font-size: 15px;
  font-weight: 700;
  color: rgba(41, 49, 72, 0.8);
  display: flex;
  align-items: center;
  gap: 8px;

  &-green {
    background-color: #7fc75e22;
    color: #7fc75e;
  }
}
</style>
