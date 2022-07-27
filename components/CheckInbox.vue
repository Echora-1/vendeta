<template>
  <div class="checkin-box">
    <icon-mail />
    <p class="form-title">Check inbox</p>
    <p class="form-subtitle">
      We sent you an email with a confirmation link to {{email}}.
      Please check the inbox and spam folder.
    </p>
    <base-button @click.native="$router.push(localePath('/log-in'))" class="checkin-box__btn"> Back to home </base-button>
  </div>
</template>
<script>
import IconMail from '@/components/icon/IconMail'
import BaseButton from '@/components/base/BaseButton'
export default {
  components: { BaseButton, IconMail },

  props: {
    email: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.form-subtitle {
  max-width: 300px;
}

.checkin-box {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__btn {
    min-width: 320px;
  }
}
</style>
