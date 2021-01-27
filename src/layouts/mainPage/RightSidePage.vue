<template>
  <section class="right-container">
    <div class="right-container__wrapper">
      <div class="right-container__auth auth-info">
        <h3 class="auth-info__tittle">Авторизация</h3>
        <p class="auth-info__subtitle">
          Если у вас уже существует аккаунт, вы можете войти в него
        </p>
      </div>
      <form class="auth-form">
        <AppInput placeholder="Логин" class="auth-form__login auth-form__login--positionlog">
          <template #left-icon>
            <AppIcon class="auth-form__login-icon">
              <icon-main-user />
            </AppIcon>
          </template>
        </AppInput>
        <AppInput placeholder="Пароль" class="auth-form__login auth-form__login--positionpas">
          <template #left-icon>
            <AppIcon class="auth-form__login-icon">
              <icon-main-lock />
            </AppIcon>
          </template>
        </AppInput>
        <div class="auth-form__prompt">
          <AppInputCheckbox class auth-form__prompt />
          <AppLink href="#" class="auth-form__prompt-password"
            >Забыли пароль?</AppLink
          >
        </div>
        <AppButton class="auth-form__button">Войти</AppButton>
        <div class="auth-form__register-link">
          <p class="auth-form__register-text">Нет аккаунта?</p>
          <AppLink href="#" color="#0075ff">Зарегистрироваться</AppLink>
        </div>
      </form>
    </div>
  </section>
</template>

<script>
import AppInput from "../../components/appComponents/AppInput";
import AppIcon from "../../components/appComponents/AppIcon";
import IconMainUser from "../../assets/icon/icon-main-user";
import IconMainLock from "../../assets/icon/icon-main-lock";
import AppInputCheckbox from "../../components/appComponents/AppInputCheckbox";
import AppButton from "../../components/appComponents/AppButton";
import AppLink from "../../components/appComponents/AppLink";
export default {
  name: "RightSidePage",
  components: {
    AppLink,
    AppButton,
    AppInputCheckbox,
    IconMainLock,
    IconMainUser,
    AppIcon,
    AppInput
  }
};
</script>

<style lang="scss" scoped>
.right-container {
  min-width: 500px;
  height: 649px;
  background-color: #ffffff;
  z-index: 100;
  border-radius: 20px;

  &__wrapper {
    width: 295px;
    margin: 97px auto 0;
  }
}

.auth-info {
  text-align: center;
  &__tittle {
    font-weight: 500;
    font-size: 24px;
    line-height: 29px;
    color: #000000;
    margin-bottom: 24px;
  }
  &__subtitle {
    line-height: 19px;
    color: #aaaaaa;
    margin-bottom: 54px;
  }
}

.auth-form {
  &__login {
    position: relative;
    color: #dedede;
    &--positionlog {
      margin-bottom: 19px;
    }
    &--positionpas {
      margin-bottom: 34px;
    }
  }
  &__login:focus-within {
    color: #0075ff;
    transition-duration: 1s;
  }
  &__login-icon {
    position: absolute;
    top: 50%;
    left: 5px;
    transform: translate(0, -50%);
  }

  &__password {
    position: relative;
  }
  &__password-icon {
    position: absolute;
  }

  &__prompt {
    display: flex;
    justify-content: space-between;
    margin-bottom: 55px;
  }
  &__prompt-password:hover {
    color: #0075ff;
  }

  &__register-link {
    display: flex;
    justify-content: space-between;
  }
  &__register-text {
    color: #aaaaaa;
    margin-left: 8px;
  }

  &__button {
    margin-bottom: 25px;
  }
}
</style>
