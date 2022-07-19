<template>
  <div class="acc-settings">
    <div class="account-header">
      <p class="account-header__title">{{ $t('headerTitle') }}</p>
      <base-notice
        v-show="showNotice"
        class="account-header__notice"
        @close="showNotice = false"
      />
    </div>
    <div class="acc-settings__main">
      <p class="acc-settings__title">{{ $t('title') }}</p>
      <div class="acc-settings__cards">
        <account-setting-card v-for="(card, index) in $t('cards')" :key="index" :content="card" class="acc-settings__card" />
      </div>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "headerTitle": "Settings",
    "title": "account settings",
    "cards": [
      {
        "icon": "IconAccount",
        "iconWidth": "60",
        "iconHeight": "59",
        "name": "Account Details",
        "title": "Email address",
        "text": "groov2r@gmail.com",
        "btn": "Reset password"
      },
      {
        "icon": "IconTwofa",
        "iconWidth": "60",
        "iconHeight": "60",
        "name": "2FA",
        "title": "Two-factor authentication",
        "text": "Disabled",
        "btn": "Enable 2FA"
      },
      {
        "icon": "IconDeletion",
        "iconWidth": "60",
        "iconHeight": "61",
        "name": "Account Deletion",
        "btn": "Delete Account"
      }
    ]
  },
  "ch": {
    "headerTitle": "Settings",
    "title": "account settings",
    "cards": [
      {
        "icon": "IconAccount",
        "iconWidth": "60",
        "iconHeight": "59",
        "name": "Account Details",
        "title": "Email address",
        "text": "groov2r@gmail.com",
        "btn": "Reset password"
      },
      {
        "icon": "IconTwofa",
        "iconWidth": "60",
        "iconHeight": "60",
        "name": "2FA",
        "title": "Two-factor authentication",
        "text": "Disabled",
        "btn": "Enable 2FA"
      },
      {
        "icon": "IconDeletion",
        "iconWidth": "60",
        "iconHeight": "61",
        "name": "Account Deletion",
        "btn": "Delete Account"
      }
    ]
  },
  "tur": {
    "headerTitle": "Settings",
    "title": "account settings",
    "cards": [
      {
        "icon": "IconAccount",
        "iconWidth": "60",
        "iconHeight": "59",
        "name": "Account Details",
        "title": "Email address",
        "text": "groov2r@gmail.com",
        "btn": "Reset password"
      },
      {
        "icon": "IconTwofa",
        "iconWidth": "60",
        "iconHeight": "60",
        "name": "2FA",
        "title": "Two-factor authentication",
        "text": "Disabled",
        "btn": "Enable 2FA"
      },
      {
        "icon": "IconDeletion",
        "iconWidth": "60",
        "iconHeight": "61",
        "name": "Account Deletion",
        "btn": "Delete Account"
      }
    ]
  }
}
</i18n>

<script>
import BaseNotice from "@/components/base/BaseNotice";
import AccountSettingCard from "@/components/account/AccountSettingCard";
export default {
  components: {AccountSettingCard, BaseNotice},

  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },
}
</script>

<style lang="scss" scoped>
.acc-settings {
  &__main {
    background: #E7F6FB;
    border-radius: 16px;
    padding: 74px 40px 64px;
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
    margin: 0 0 36px;
  }

  &__cards {
    max-width: 830px;
    width: 100%;
    display: flex;
  }

  &__card {
    width: calc((100% - 50px) / 3);

    &:not(:last-child) {
      margin-right: 25px;
    }
  }
}
</style>
