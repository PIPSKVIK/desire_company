<template>
  <button :type="type" class="btn">
    <slot />
  </button>
</template>

<script>
export default {
  name: "AppButton",

  props: {
    type: {
      type: String,
      default: "button"
    }
  }
};
</script>

<style lang="scss" scoped>
.btn {
  border: none;
  outline: none;
  background-color: #0075ff;
  border-radius: 83px;
  color: #ffffff;
  padding: 10px 124px;
  cursor: pointer;

  &:hover {
    background-color: #0043a4;
    transition-duration: 1s;
  }
}
</style>
