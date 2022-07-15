<template>
  <div class="faq-block container">
    <h2 class="base-title">FAQ</h2>
    <div class="faq-block__list">
      <base-accordion
        v-for="(item, index) in $t('questions')"
        :key="index"
        :content="item"
        class="faq-block__item"
      />
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
import BaseAccordion from "@/components/base/BaseAccordion";
export default {
  components: {BaseAccordion}
}
</script>


<style lang="scss" scoped>
.base-title {
  margin-bottom: 30px;
}

.faq-block {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__list {
    width: 816px;
  }

  &__item {
    &:not(:last-child) {
      margin-bottom: 15px;
    }
  }
}
</style>
