<template>
  <div class="plan-block container">
    <h1 class="base-title">{{$t('title')}}</h1>
    <p class="base-subtitle">{{$t('subtitle')[0]}}<br />
     <span>{{$t('subtitle')[1]}}</span></p>
    <div class="plan-block__plans">
      <plan-card v-for="(plan, index) in $t('plans')" :key="index" :content="plan" class="plan-block__plan"  />
    </div>
    <div class="plan-block__pay">
      <p>{{ $t('pay') }}:</p>
      <img src="../../assets/img/pay/visa.svg" width="45" height="17" alt="visa">
      <img src="../../assets/img/pay/mastercard.svg" width="45" height="27" alt="mastercard">
      <img src="../../assets/img/pay/tether.png" width="92" height="29" alt="tether">
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "title": "Order VPN",
    "pay": "Pay with",
    "subtitle": [
      "VENDETA`s nanopayments mean you are never locked into a subscription and pay only for actual use.",
      "Choose your plan and start browsing."
    ],
    "plans": [
      {
        "duration": "12 months",
        "icon": "crystal",
        "price": "1.75",
        "sum": "42"
      }
    ]
  },
  "ch": {
    "title": "Order VPN",
    "pay": "Pay with",
    "subtitle": [
      "VENDETA`s nanopayments mean you are never locked into a subscription and pay only for actual use.",
      "Choose your plan and start browsing."
    ],
    "plans": [
      {
        "duration": "12 months",
        "icon": "crystal",
        "price": "1.75",
        "sum": "42"
      }
    ]
  },
  "tur": {
    "title": "Order VPN",
    "pay": "Pay with",
    "subtitle": [
      "VENDETA`s nanopayments mean you are never locked into a subscription and pay only for actual use.",
      "Choose your plan and start browsing."
    ],
    "plans": [
      {
        "duration": "12 months",
        "icon": "crystal",
        "price": "1.75",
        "sum": "42"
      }
    ]
  }
}
</i18n>

<script>
import PlanCard from "@/components/plans/PlanCard";
export default {
  components: {PlanCard}
}
</script>

<style lang="scss" scoped>

.base-title {
  margin: 7px 0 0;
}

.base-subtitle {
  max-width: 820px;
  text-align: center;
  color: black;
  margin-bottom: 46px;

  span {
    font-weight: bold;
  }
}

.plan-block {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__plans {
    max-width: 944px;
    width: 100%;
    display: flex;
    justify-content: center;
    padding-bottom: 55px;
  }

  &__plan {
    width: 100%;
    max-width: calc((944px - 32px) / 2 );

    &:not(:first-child) {
      margin-left: 32px;
    }
  }

  &__pay {
    display: flex;
    justify-content: center;
    align-items: center;

    p {
      font-size: 18px;
      line-height: 26px;
      text-align: center;
      color: #000000;
      opacity: 0.7;
      margin: 0 22px 0 0;
      display: inline-block;
    }

    img {
      object-fit: contain;

      &:not(:last-child) {
        margin-right: 40px;
      }
    }
  }
}
</style>

