<template>
  <div class="main">
    <div class="main__container">
      <LeftSidePage />
      <RightSidePage class="main__container-left" />
    </div>
  </div>
</template>

<script>
import LeftSidePage from "./mainPage/LeftSidePage";
import RightSidePage from "./mainPage/RightSidePage";
export default {
  name: "MainLayout",
  components: { LeftSidePage, RightSidePage }
};
</script>

<style lang="scss" scoped>
.main {
  width: 100vw;
  height: 100vh;
  z-index: -1;
  background-image: url("../assets/image/main-background-image.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;

  &__container {
    width: 933px;
    display: flex;
    position: relative;

    &-left {
      position: absolute;
      right: 0;
    }
  }
}
</style>
