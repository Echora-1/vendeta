<template>
  <div class="container">
    <div class="account-block">
      <account-tabs>
        <base-tab :title="$t('nav')[0].title">
          <account-overview class="account-block__nav-item" />
        </base-tab>
        <base-tab :title="$t('nav')[1].title">
          <account-downloads class="account-block__nav-item" />
        </base-tab>
        <base-tab :title="$t('nav')[2].title">
          <account-biling class="account-block__nav-item" />
        </base-tab>
        <base-tab :title="$t('nav')[3].title">
          <account-settings class="account-block__nav-item" />
        </base-tab>
        <base-tab :title="$t('nav')[4].title">
          <account-help class="account-block__nav-item" />
        </base-tab>
      </account-tabs>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "nav": [
      {
        "title": "Overview"
      },
      {
        "title": "Downloads"
      },
      {
        "title": "Billing"
      },
      {
        "title": "Settings"
      },
      {
        "title": "Help Center"
      }
    ]
  },
  "ch": {
    "nav": [
      {
        "title": "Overview"
      },
      {
        "title": "Downloads"
      },
      {
        "title": "Billing"
      },
      {
        "title": "Settings"
      },
      {
        "title": "Help Center"
      }
    ]
  },
  "tur": {
    "nav": [
      {
        "title": "Overview"
      },
      {
        "title": "Downloads"
      },
      {
        "title": "Billing"
      },
      {
        "title": "Settings"
      },
      {
        "title": "Help Center"
      }
    ]
  }
}
</i18n>

<script>
import AccountTabs from '@/components/account/AccountTabs'
import BaseTab from '@/components/base/BaseTab'
import AccountOverview from '@/components/account/AccountOverview'
import AccountDownloads from '@/components/account/AccountDownloads'
import AccountBiling from '@/components/account/AccountBiling'
import AccountSettings from '@/components/account/AccountSettings'
import AccountHelp from '@/components/account/AccountHelp'
export default {
  components: {
    AccountHelp,
    AccountSettings,
    AccountBiling,
    AccountDownloads,
    AccountOverview,
    BaseTab,
    AccountTabs,
  },
}
</script>

<style lang="scss" scoped>
.account-block {
  min-height: 820px;
  background: #ffffff;
  border-radius: 30px;

  &__nav-item {
    padding: 38px 68px;
  }
}
</style>
