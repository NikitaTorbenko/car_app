<script setup></script>

<template>
  <footer class="footer">
    <div class="footer-left-side">Showing 9 out of 256</div>
    <div class="pagination">
      <img
        class="chevron chevron-left"
        src="../assets/icons/chevron.svg"
        alt=""
      />
      <div class="pagination-page">1</div>
      <div class="pagination-text">of</div>
      <div class="pagination-page pagination-page-total">28</div>
      <img
        class="chevron chevron-right"
        src="../assets/icons/chevron.svg"
        alt=""
      />
    </div>
  </footer>
</template>

<style scoped lang="scss">
.footer {
  margin: 32px 0 45px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &-left-side {
    color: rgba(41, 49, 72, 0.8);
    font-size: 16px;
  }

  @media (max-width: 680px) {
    flex-direction: column;
    gap: 30px;
  }
}

.pagination {
  display: flex;
  align-items: center;
  gap: 12px;

  &-page {
    width: 32px;
    height: 32px;
    line-height: 2;
    border-radius: 6px;
    border: 1px solid #e4e4e4;
    color: rgba(41, 49, 72, 0.8);
    text-align: center;
    font-size: 15px;

    &-total {
      color: rgba(41, 49, 72, 0.45);
    }
  }

  &-text {
    color: rgba(41, 49, 72, 0.8);
    text-align: center;
    font-size: 13px;
  }
}

.chevron {
  cursor: pointer;

  &-left {
    transform: rotate(90deg);
  }
  &-right {
    transform: rotate(270deg);
  }
}
</style>
