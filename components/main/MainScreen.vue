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
      <vpn-app />
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

  @media(max-width: 1000px) {
    min-width: 269px;
  }

  @media(max-width: 767px) {
    max-width: 275px;
    text-align: center;
  }

}

.base-subtitle {
  max-width: 475px;
  margin-bottom: 44px;

    @media(max-width: 767px) {
    max-width: 330px;
    text-align: center;
    margin-bottom: 24px;
  }
}

.maim-screen {
  display: flex;
  padding-top: 181px;

  @media(max-width: 1000px) {
    padding-top: 140px;
  }

  @media(max-width: 767px) {
    padding-top: 15px;
  }

  &__left,
  &__right {
    @media(min-width: 1001px) {
      flex: 0 0 50%;
      max-width: 50%;
    }
  }

  &__left {
    padding-top: 62px;

    @media(min-width: 1001px) {
      padding-right: 16px;
    }

    @media(max-width: 767px) {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
    }

  }

  &__right {
    @media(min-width: 1001px) {
      padding-left: 16px;
    }

    @media(max-width: 767px) {
      display: none;
    }
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

    @media(max-width: 1000px) {
      margin-bottom: 20px;
    }
  }
}

.action {
  display: flex;
  align-items: center;

  @media(max-width: 1000px) {
    flex-direction: column-reverse;
    align-items: flex-start;
  }

  @media(min-width: 769px) {
    margin-right: 20px;
  }

  @media(max-width: 767px) {
    align-items: center;
  }

  &__btn {
    @media(min-width: 769px) {
      margin-right: 20px;
    }
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


  @media(min-width: 1001px) {
    align-items: center;
  }

  @media(max-width: 1000px) {
    flex-direction: column;
  }

  @media(max-width: 767px) {
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: center;
  }

  &__icon {
    @media(min-width: 1001px) {
      margin-left: 21px;

      &:last-child {
        margin-left: 39px;
      }
    }

    @media(max-width: 1000px) {
      margin-bottom: 20px;
    }

    @media(max-width: 767px) {
      width: 50%;
    }
  }

  &__text {
    font-size: 18px;
    line-height: 26px;
    opacity: 0.7;

    @media(max-width: 767px) {
      width: 60%;
      text-align: center;
    }
  }
}
</style>
<script>
import BaseButton from '~/components/base/BaseButton'
import IconAndroid from '~/components/icon/IconAndroid'
import IconWindows from '~/components/icon/IconWindows'
import VpnApp from "@/components/main/VpnApp";
export default {
  components: {VpnApp, IconWindows, IconAndroid, BaseButton },
}
</script>
