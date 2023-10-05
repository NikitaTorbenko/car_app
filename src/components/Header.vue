<script setup>
const countOfCars = 256;
</script>

<template>
  <header class="header">
    <div class="left-side">
      <h1 class="title">Vechicles</h1>
      <div class="count-block">{{ countOfCars }}</div>
    </div>
    <div class="right-side">
      <div class="plus">
        <img src="../assets/icons/plus.svg" alt="" />
      </div>
      <div class="profile-block">
        <div class="profile-block-icon"></div>
        <div class="profile-block-name">John Doe</div>
      </div>
      <div class="language-block">
        <img src="../assets/img/flag.png" alt="" class="language-icon" />
        <span class="language">En</span>
        <img class="chevron" src="../assets/icons/chevron.svg" alt="" />
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  padding: 30px;
  grid-area: header;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.1);

  @media (max-width: 850px) {
    flex-direction: column;
  }
}

.left-side {
  display: flex;
  align-items: center;
  gap: 18px;
  @media (max-width: 850px) {
    margin-bottom: 20px;
  }
}

.title {
  font-size: 32px;
  font-weight: 700;
}

.count-block {
  padding: 4px 14px;
  font-size: 15px;
  font-weight: 700;
  color: rgba(41, 49, 72, 0.8);
  border-radius: 6px;
  background-color: #f3f6f8;
}

.right-side {
  display: flex;
  align-items: center;
}

.plus {
  cursor: pointer;
  padding: 9px;
  border-radius: 6px;
  border: 1px solid #e86e84;
}

.profile-block {
  margin-left: 40px;
  margin-right: 32px;
  display: flex;
  align-items: center;
  gap: 14px;

  &-icon {
    width: 46px;
    height: 46px;
    border-radius: 50%;
    background-image: url('../assets/img/user.jpg');
  }

  &-name {
    color: #293148;
    font-size: 15px;
    font-weight: 700;
  }

  @media (max-width: 880px) {
    margin-left: 20px;
    margin-right: 16px;
  }
}

.language {
  font-size: 15px;
  font-weight: 700;
  margin-left: 14px;
  margin-right: 3px;

  &-block {
    display: flex;
    align-items: center;
  }
}

.chevron {
  transition: 0.5s;
  &:hover {
    transform: rotate(180deg);
  }
}
</style>
