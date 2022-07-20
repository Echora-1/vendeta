<template>
  <div class="acc-help">
    <div class="account-header">
      <p class="account-header__title">Help Center</p>
      <base-notice
        v-show="showNotice"
        class="account-header__notice"
        @close="showNotice = false"
      />
    </div>
    <div class="acc-help__main" >
      <vertical-tabs title="category">
        <base-tab title="General info" class="acc-help__main-item">
          <base-accordion
            v-for="(item, index) in $t('questions')"
            :key="index"
            :content="item"
            class="acc-help__accordion"
          />
        </base-tab>
        <base-tab title="Billing" class="acc-help__main-item">

        </base-tab>
        <base-tab title="Connectivity" class="acc-help__main-item">

        </base-tab>
      </vertical-tabs>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "questions":[
      {
        "title":"How do I buy a VendetaVPN key?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How much does a VPN cost?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Can I buy VendetaVPN for USDT?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How do I upgrade my plan?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Do you accept BankCard payments?",
        "text":[
          "Answer."
        ]
      }
    ]
  },
  "ch": {
    "questions":[
      {
        "title":"How do I buy a VendetaVPN key?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How much does a VPN cost?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Can I buy VendetaVPN for USDT?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How do I upgrade my plan?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Do you accept BankCard payments?",
        "text":[
          "Answer."
        ]
      }
    ]
  },
  "tur": {
    "questions":[
      {
        "title":"How do I buy a VendetaVPN key?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How much does a VPN cost?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Can I buy VendetaVPN for USDT?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"How do I upgrade my plan?",
        "text":[
          "Answer."
        ]
      },
      {
        "title":"Do you accept BankCard payments?",
        "text":[
          "Answer."
        ]
      }
    ]
  }
}
</i18n>

<script>
import BaseNotice from "@/components/base/BaseNotice";
import VerticalTabs from "@/components/account/VerticalTabs";
import BaseTab from "@/components/base/BaseTab";
import BaseAccordion from "@/components/base/BaseAccordion";
export default {
  components: {BaseAccordion, BaseTab, BaseNotice, VerticalTabs},

  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },

}
</script>

<style lang="scss" scoped>
::v-deep .tab-label,
::v-deep .tab-content {
  background: #E7F6FB;
}

.acc-help {
  &__main-item {
    width: 100%;
  }

  &__accordion {
    &:not(:last-child) {
      margin-bottom: 15px;
    }
  }
}
</style>
