<template>
  <div class="acc-downloads">
    <div class="account-header">
      <p class="account-header__title">{{ $t('headerTitle') }}</p>
      <base-notice
        v-show="showNotice"
        class="account-header__notice"
        @close="showNotice = false"
      />
    </div>
    <div class="acc-downloads__main">
        <p class="acc-downloads__title">{{ $t('title') }}</p>
        <div class="acc-downloads__type">
          <div class="acc-downloads__type-item">
              <p>{{ $t('mobile') }}</p>
              <div></div>
          </div>
          <div class="acc-downloads__type-item">
            <p>{{ $t('pc') }}</p>
            <div></div>
          </div>
        </div>
      <div class="acc-downloads__platform">
        <account-downlod-card v-for="(card, index) in $t('cards')" :key="index" :content="card" class="acc-downloads__platform-item" />
      </div>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "headerTitle": "Downloads",
    "title": "choose your device os and download",
    "mobile": "Mobile",
    "pc": "PC",
    "cards": [
      {
        "icon": "IconLogoAndroid",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Android",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoIOS",
        "iconWidth": "50",
        "iconHeight": "61",
        "platform": "iOS",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoMacos",
        "iconWidth": "60",
        "iconHeight": "60",
        "platform": "Mac OS",
        "ver": "Ver 1.01",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoWindows",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Windows",
        "ver": "Ver 7.2-37",
        "update": "(updated 18.07.22)"
      }
    ]
  },
  "ch": {
    "headerTitle": "Downloads",
    "title": "choose your device os and download",
    "mobile": "Mobile",
    "pc": "PC",
    "cards": [
      {
        "icon": "IconLogoAndroid",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Android",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoIOS",
        "iconWidth": "50",
        "iconHeight": "61",
        "platform": "iOS",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoMacos",
        "iconWidth": "60",
        "iconHeight": "60",
        "platform": "Mac OS",
        "ver": "Ver 1.01",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoWindows",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Windows",
        "ver": "Ver 7.2-37",
        "update": "(updated 18.07.22)"
      }
    ]
  },
  "tur": {
    "headerTitle": "Downloads",
    "title": "choose your device os and download",
    "mobile": "Mobile",
    "pc": "PC",
    "cards": [
      {
        "icon": "IconLogoAndroid",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Android",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoIOS",
        "iconWidth": "50",
        "iconHeight": "61",
        "platform": "iOS",
        "ver": "Ver 7.2-37",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoMacos",
        "iconWidth": "60",
        "iconHeight": "60",
        "platform": "Mac OS",
        "ver": "Ver 1.01",
        "update": "(updated 16.07.22)"
      },
      {
        "icon": "IconLogoWindows",
        "iconWidth": "48",
        "iconHeight": "57",
        "platform": "Windows",
        "ver": "Ver 7.2-37",
        "update": "(updated 18.07.22)"
      }
    ]
  }
}
</i18n>

<script>
import BaseNotice from "@/components/base/BaseNotice";
import AccountDownlodCard from "@/components/account/AccountDownlodCard";
export default {
  components: {AccountDownlodCard, BaseNotice},

  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },
}
</script>

<style lang="scss" scoped>
.acc-downloads {
  &__main {
    background: #E7F6FB;
    border-radius: 16px;
    padding: 43px 40px 64px;
    min-height: 550px;
    max-width: 1090px;
    width: 100%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    flex-direction: column;
  }

  &__title {
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    color: #576280;
    opacity: 0.4;
    text-transform: uppercase;
    margin: 0 0 30px;
  }

  &__type {
    display: flex;
    justify-content: space-around;
    max-width: 940px;
    width: 100%;
  }

  &__type-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 25.5%;

    p {
      font-weight: 500;
      font-size: 14px;
      line-height: 20px;
      color: #576280;
      margin: 0 0 10px;
    }

    div  {
      max-width: 240px;
      width: 100%;
      height: 30px;
      opacity: 0.2;
      background: transparent;
      border-top: 1px solid #576280;
      border-left: 1px solid transparent;
      border-right: 1px solid transparent;
      position: relative;

      &::before,
      &::after {
        content: "";
        position: absolute;
        width: 30px;
        height: 1px;
        background: linear-gradient(90deg, #576280 -1.67%, rgba(87, 98, 128, 0) 100%);
        transform: rotate(90deg);
      }

      &::before {
        top: 14px;
        left: -15px;
      }

      &::after {
        top: 14px;
        right: -15px;
      }
    }
  }

  &__platform {
    display: flex;
    width: 100%;
    max-width: 940px;
  }

  &__platform-item {
    width: calc((100% - 60px) / 4);

    &:not(:last-child) {
      margin-right: 20px;
    }
  }
}
</style>
