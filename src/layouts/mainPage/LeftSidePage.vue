<template>
  <section class="left-container">
    <div class="left-content left-background">
      <div class="left-content__wrapper">
        <h1 class="left-content__title">Desire RolePlay</h1>
        <p class="left-content__subtitle">
          Лучший проект игровых серверов за всю историю GTA V
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "LeftSidePage"
};
</script>

<style lang="scss" scoped>
.left-container {
  width: 489px;
  height: 649px;
  background-image: url("../../assets/image/left-side-page-background.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  color: #ffffff;
  text-align: center;
}
.left-content {
  display: flex;
  &__wrapper {
    width: 269px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0 auto 0 92px;
    text-align: start;
    padding-bottom: 52px;
  }
  &__title {
    font-weight: bold;
    font-size: 54px;
    line-height: 65px;
    margin-bottom: 13px;
  }
  &__subtitle {
    line-height: 19px;
  }
}

.left-background {
  background-color: rgba(0, 117, 255, 0.85);
  width: 489px;
  height: 649px;
  border-radius: 20px;
}
</style>
