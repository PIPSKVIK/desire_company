<template>
  <component
    :is="tag"
    class="link"
    :style="colorType"
    v-on="$listeners"
    v-bind="$attrs"
  >
    <slot />
  </component>
</template>

<script>
export default {
  name: "AppLink",

  props: {
    tag: {
      type: String,
      default: "a"
    },
    color: {
      type: String,
      default: "#aaaaaa"
    }
  },

  computed: {
    colorType() {
      return {
        color: this.color
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.link {
  text-decoration: none;
}
</style>
