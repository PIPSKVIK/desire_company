<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="width"
    :height="height"
    :viewBox="viewBox"
    :aria-labelledby="iconName"
  >
    <g :fill="iconColor">
      <slot />
    </g>
  </svg>
</template>

<script>
export default {
  name: "AppIcon",

  props: {
    width: {
      type: [String, Number],
      default: 18
    },
    height: {
      type: [String, Number],
      default: 18
    },
    iconColor: {
      type: String,
      default: "currentColor"
    },
    iconName: {
      type: String,
      default: "icon"
    },
    viewBox: {
      type: [String, Number],
      default: "0 0 18 18"
    }
  }
};
</script>

<style scoped></style>
