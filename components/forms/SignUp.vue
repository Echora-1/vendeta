<template>
  <div class="sign-up-form">
    <h2 class="form-title">Create an account</h2>
    <p class="form-subtitle">
      Already have an account?
      <nuxt-link :to="localePath('/log-in')"> Log in </nuxt-link>
    </p>
    <form class="sign-up-form__form">
      <base-input
        v-model="email"
        name="email"
        class="sign-up-form__input"
        placeholder="Your Email Adress"
        :invalid="emailInvalid"
        required-field
        @input="emailInvalid = false"
      />
      <base-button class="sign-up-form__btn" type="submit">
        Continue
      </base-button>
    </form>
    <p class="sign-up-form__text">
      By signing up, you agree with our
      <nuxt-link :to="localePath('')">Terms of Service</nuxt-link> and
      <nuxt-link :to="localePath('')">Privacy Policy</nuxt-link>.
    </p>
    <base-button class="sign-up-form__btn sign-up-form__btn-google">
      <icon-google /> Sign up with Google </base-button>
  </div>
</template>

<script>
import BaseInput from '@/components/base/BaseInput'
import BaseButton from '@/components/base/BaseButton'
import IconGoogle from "@/components/icon/IconGoogle";
export default {
  components: {IconGoogle, BaseButton, BaseInput },

  data() {
    return {
      email: '',
      emailInvalid: false,
    }
  },
}
</script>

<style lang="scss" scoped>
.sign-up-form {
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

  &__text {
    font-size: 14px;
    line-height: 22px;
    text-align: center;
    margin: 0 0 40px;
    color: #576280;
    max-width: 320px;

    a {
      text-decoration: underline;
    }
  }

  &__btn-google {
    background: #E7F6FB;
    border-color: #E7F6FB;
    color: #576280;

    svg {
      margin-right: 9px;
    }
  }
}
</style>
