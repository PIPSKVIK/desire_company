<template>
  <div>
    <slot name="left-icon" />
    <input
      class="form-control"
      v-bind="$attrs"
      v-on="listeners"
      :class="classIcon"
      :type="type"
    />
  </div>
</template>

<script>
export default {
  name: "AppInput",

  inheritAttrs: false,

  props: {
    value: {},
    type: {
      type: String,
      default: "text"
    }
  },

  model: {
    prop: "value",
    event: "input"
  },

  data() {
    return {
      iconLeft: false
    };
  },

  mounted() {
    this.updateIcon();
  },

  methods: {
    updateIcon() {
      this.iconLeft = !!this.$slots["left-icon"];
    }
  },

  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: $event => {
          this.$emit("input", $event.target.value);
        },
        change: $event => {
          this.$emit("change", $event.target.value);
        }
      };
    },

    classIcon() {
      return {
        "input-group_icon-left": this.iconLeft
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.form-control {
  border: none;
  outline: none;
  width: 295px;
  color: rgba(222, 222, 222, 1);
  border-bottom: 2px solid rgba(222, 222, 222, 1);

  &:focus {
    color: #0075ff;
    border-bottom-color: #0075ff;
    transition-duration: 1s;
  }
}
.input-group_icon-left {
  padding: 8px 0 8px 30px;
}

input::placeholder {
  color: #595959;
  font-size: 18px;
}
</style>
