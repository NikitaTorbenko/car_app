<script setup>
defineProps({
  className: {
    type: String,
    required: false,
  },
  icon: {
    type: String,
    required: false,
  },
  text: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <button :class="`btn ${className}`">
    <img :src="icon" v-if="icon" alt="" class="icon" />
    {{ text }}
  </button>
</template>

<style scoped lang="scss">
.btn {
  border-radius: 10px;
  width: fit-content;
  height: fit-content;
  display: flex;
  align-items: center;
  padding: 9px 18px;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.icon {
  margin-right: 16px;
}
</style>
