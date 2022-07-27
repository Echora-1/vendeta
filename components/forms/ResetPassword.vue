<template>
  <div class="reset-pass-form">
    <h2 class="form-title"> Reset password</h2>
    <p class="form-subtitle">
      Enter your email address, and we’ll send you a link to reset your password.
    </p>
    <form class="reset-pass-form__form">
      <base-input
        v-model="email"
        name="email"
        class="reset-pass-form__input"
        placeholder="Username or email adress"
        :invalid="emailInvalid"
        required-field
        @input="emailInvalid = false"
      />
    </form>
    <base-button class="reset-pass-form__btn" @click.native="submit">
      Send
    </base-button>
    <nuxt-link :to="localePath('/log-in')" class="reset-pass-form__link">
      Back to log in
    </nuxt-link>
  </div>
</template>

<script>
import BaseInput from '@/components/base/BaseInput'
import BaseButton from '@/components/base/BaseButton'
export default {
  components: { BaseButton, BaseInput },

  data() {
    return {
      email: '',
      emailInvalid: false,
    }
  },

  methods: {
    submit: function submit() {
      this.$emit('submitForm', this.email)
    },
  },
}
</script>

<style lang="scss" scoped>
.form-subtitle {
  max-width: 290px;
  font-size: 16px;
  line-height: 22px;
}

.reset-pass-form {
  display: flex;
  align-items: center;
  flex-direction: column;

  &__input {
    min-width: 320px;
  }

  &__btn {
    min-width: 320px;
    margin-bottom: 27px;
  }

  &__link {
    font-size: 14px;
    line-height: 22px;
    color: #00B4DB;
    text-decoration: underline;
  }
}
</style>
