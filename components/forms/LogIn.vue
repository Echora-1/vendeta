<template>
  <div class="log-in-form">
    <h2 class="form-title">Log in</h2>
    <p class="form-subtitle">
      Don’t have an account?
      <nuxt-link :to="localePath('/sign-up')"> Sign Up </nuxt-link>
    </p>
    <form class="log-in-form__form">
      <base-input
        v-model="email"
        name="email"
        class="log-in-form__input"
        placeholder="Username or email adress"
        :invalid="emailInvalid"
        required-field
        @input="emailInvalid = false"
      />
      <base-button class="log-in-form__btn" type="submit"> Continue </base-button>
    </form>
    <nuxt-link :to="localePath('/reset-password')" class="log-in-form__link">
      Forgot your password?
    </nuxt-link>
    <base-button class="log-in-form__btn log-in-form__btn-google">
      <icon-google /> Sign up with Google
    </base-button>
  </div>
</template>

<script>
import BaseInput from '@/components/base/BaseInput'
import BaseButton from '@/components/base/BaseButton'
import IconGoogle from '@/components/icon/IconGoogle'
export default {
  components: { IconGoogle, BaseButton, BaseInput },

  data() {
    return {
      email: '',
      emailInvalid: false,
    }
  },
}
</script>

<style lang="scss" scoped>
.log-in-form {
  display: flex;
  align-items: center;
  flex-direction: column;

  &__input {
    min-width: 320px;
  }

  &__btn {
    min-width: 320px;
  }

  &__form {
    margin-bottom: 27px;
  }

  &__btn-google {
    background: #e7f6fb;
    border-color: #e7f6fb;
    color: #576280;

    svg {
      margin-right: 9px;
    }
  }

  &__link {
    font-size: 14px;
    line-height: 22px;
    color: #00b4db;
    text-decoration: underline;
    margin-bottom: 62px;
  }
}
</style>
