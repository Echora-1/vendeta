<template>
  <div class="container">
    <div class="account-block">
      <account-tabs>
        <base-tab :title="$t('nav')[0].title">
          <overview-block class="account-block__nav-item" />
        </base-tab>
        <base-tab :title="$t('nav')[1].title"></base-tab>
        <base-tab :title="$t('nav')[2].title"></base-tab>
        <base-tab :title="$t('nav')[3].title"></base-tab>
        <base-tab :title="$t('nav')[4].title"></base-tab>
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
import AccountTabs from "@/components/account/AccountTabs";
import BaseTab from "@/components/base/BaseTab";
import OverviewBlock from "@/components/account/OverviewBlock";
export default {
  components: {OverviewBlock, BaseTab, AccountTabs}
}
</script>

<style lang="scss" scoped>
.account-block {
  min-height: 820px;
  background: #FFFFFF;
  border-radius: 30px;

  &__nav-item {
    padding: 38px 68px;
  }
}
</style>
