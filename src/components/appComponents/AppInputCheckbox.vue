<template>
  <div>
    <input
      type="checkbox"
      class="checkbox"
      id="remember"
      name="remember"
      v-model="active"
    />
    <label for="remember" :class="classElement">Запомнить</label>
  </div>
</template>

<script>
export default {
  name: "AppInputCheckbox",

  data() {
    return {
      active: false,
      inactive: false
    };
  },

  computed: {
    classElement() {
      return {
        "label-active": this.active,
        "label-inactive": this.inactive
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.checkbox {
  position: absolute;
  z-index: -1;
  opacity: 0;
}

.checkbox + label {
  display: inline-flex;
  align-items: center;
  user-select: none;
}
.checkbox + label::before {
  content: "";
  display: inline-block;
  width: 1em;
  height: 1em;
  flex-shrink: 0;
  flex-grow: 0;
  border: 2px solid #adb5bd;
  border-radius: 4px;
  margin-right: 13px;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 50% 50%;
}

.checkbox:checked + label::before {
  border-color: #0b76ef;
  background-color: #0b76ef;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3e%3cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3e%3c/svg%3e");
}

label {
  color: #999999;
}

label:hover {
  color: #999999;
}

.checkbox:active {
  background-color: #b3d7ff;
  border-color: #b3d7ff;
  color: #0b76ef;
}

.checkbox:not(:disabled):not(:checked) + label:hover::before {
  border-color: #0075ff;
}

.label-active {
  color: #0075ff;
}

.label-inactive {
  color: #999999;
}
</style>
