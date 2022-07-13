<template>
  <div class="maim-screen container">
    <div class="maim-screen__left">
      <h1 class="base-title-h1">{{ $t('title') }}</h1>
      <p class="base-subtitle">{{ $t('subtitle') }}</p>
      <div class="maim-screen__action action">
        <nuxt-link :to="localePath('/')">
          <base-button class="action__btn">
            {{ $t('actionBtn') }}
          </base-button>
        </nuxt-link>
        <p class="action__text">
          ️{{ $t('actionText')[0] }}<span>{{ $t('actionText')[1] }}</span>
        </p>
      </div>
      <div class="maim-screen__platform platform">
        <p class="platform__text">{{ $t('platformText') }}</p>
        <icon-android class="platform__icon" />
        <icon-windows class="platform__icon" />
      </div>
    </div>
    <div class="maim-screen__right">
      <img
        src="../../assets/img/main/main-screen-phone2x.png"
        class="maim-screen__img"
        width="487"
        height="693"
        alt="phone"
      />
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "title": "Open network for everyone",
    "subtitle": "Secure your data by tunneling it between blockhain nodes & encrypting it with variable quantum-secure encryption.",
    "actionBtn": "Get VND key",
    "actionText": ["️‍🔥️‍first 100 keys ", "for $25!"],
    "platformText": "Available for:"
  },
  "ch": {
    "title": "Open network for everyone",
    "subtitle": "Secure your data by tunneling it between blockhain nodes & encrypting it with variable quantum-secure encryption.",
    "actionBtn": "Get VND key",
    "actionText": ["️‍🔥️‍first 100 keys ", "for $25!"],
    "platformText": "Available for:"
    },
  "tur": {
    "title": "Open network for everyone",
    "subtitle": "Secure your data by tunneling it between blockhain nodes & encrypting it with variable quantum-secure encryption.",
    "actionBtn": "Get VND key",
    "actionText": ["️‍🔥️‍first 100 keys ", "for $25!"],
    "platformText": "Available for:"
  }
}
</i18n>

<style lang="scss" scoped>
.base-title-h1 {
  max-width: 480px;
  margin-bottom: 21px;
}

.base-subtitle {
  max-width: 475px;
  margin-bottom: 44px;
}

.maim-screen {
  display: flex;
  padding-top: 181px;

  &__left,
  &__right {
    flex: 0 0 50%;
    max-width: 50%;
  }

  &__left {
    padding-right: 16px;
    padding-top: 62px;
  }

  &__right {
    padding-left: 16px;
  }

  &__img {
    position: relative;
    left: -28px;
    width: 487px;
    height: 693px;
    object-fit: contain;
  }

  &__action {
    margin-bottom: 51px;
  }
}

.action {
  display: flex;
  align-items: center;

  &__btn {
    margin-right: 20px;
  }

  &__text {
    font-weight: 500;
    font-size: 20px;
    line-height: 36px;

    span {
      color: #00b4db;
    }
  }
}

.platform {
  display: flex;
  align-items: center;

  &__text {
    font-size: 18px;
    line-height: 26px;
    opacity: 0.7;
  }

  &__icon {
    margin-left: 21px;

    &:last-child {
      margin-left: 39px;
    }
  }
}
</style>
<script>
import BaseButton from '~/components/base/BaseButton'
import IconAndroid from '~/components/icon/IconAndroid'
import IconWindows from '~/components/icon/IconWindows'
export default {
  components: { IconWindows, IconAndroid, BaseButton },
}
</script>
