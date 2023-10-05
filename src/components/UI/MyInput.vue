<script setup>
defineProps({
  value: {
    type: String,
    required: true,
  },
  placeholder: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
    required: false,
    default: '',
  },
  className: {
    type: String,
    required: false,
  },
  modelValue: [String, Number],
});

const emit = defineEmits(['update:modelValue']);
const updateInput = event => {
  emit('update:modelValue', event.target.value);
};
</script>

<template>
  <div :class="`input-wrap ${className}`">
    <input
      :value="modelValue"
      @input="updateInput"
      class="input"
      type="text"
      :placeholder="placeholder"
    />
    <img v-if="icon" class="icon" :src="icon" alt="" />
  </div>
</template>

<style scoped lang="scss">
.input-wrap {
  width: fit-content;
  height: fit-content;
  border-radius: 8px;
  border: 1px solid #e4e4e4;
  position: relative;
  padding: 9px 16px;
}

.input {
  width: 90%;
  outline: none;
  font-size: 16px;

  &::placeholder {
    color: rgba(41, 49, 72, 0.8);
    font-size: 16px;
    font-weight: 400;
  }
}

.icon {
  position: absolute;
  top: 9px;
  right: 16px;
}
</style>
