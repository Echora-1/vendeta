<template>
  <div class="acc-biling">
    <div class="account-header">
      <p class="account-header__title">{{ $t('headerTitle') }}</p>
      <base-notice
        v-show="showNotice"
        class="account-header__notice"
        @close="showNotice = false"
      />
    </div>
    <div class="acc-biling__main">
      <div class="acc-biling__order">
        <icon-order />
        <p>Order key</p>
        <span>pay with cryptocurrency (USDT)</span>
        <base-button class="acc-biling__order-btn">
          Order now
          <icon-arrow-next />
        </base-button>
        <nuxt-link :to="localePath('')">
          How to pay?
        </nuxt-link>
      </div>
      <div class="acc-biling__history">
        <p class="acc-biling__title">my order history</p>
        <base-table class="acc-biling__history-table" :data="$t('table')" />
      </div>
    </div>
  </div>
</template>

<i18n>
{
  "en": {
    "headerTitle" : "Biling",
    "table": {
      "th": ["Date/time", "Type", "Amount"],
      "td": [["18/07/2022 15:47:50", "Crypto", "25.00 USDT"], ["15/06/2021 10:25:46", "Crypto", "25.00 USDT"]]
    }
  },
  "ch": {
    "headerTitle" : "Biling",
    "table": {
      "th": ["Date/time", "Type", "Amount"],
      "td": [["18/07/2022 15:47:50", "Crypto", "25.00 USDT"], ["15/06/2021 10:25:46", "Crypto", "25.00 USDT"]]
    }
  },
  "tur": {
    "headerTitle" : "Biling",
    "table": {
      "th": ["Date/time", "Type", "Amount"],
      "td": [["18/07/2022 15:47:50", "Crypto", "25.00 USDT"], ["15/06/2021 10:25:46", "Crypto", "25.00 USDT"]]
    }
  }
}
</i18n>

<script>
import BaseNotice from "@/components/base/BaseNotice";
import IconOrder from "@/components/icon/IconOrder";
import IconArrowNext from "@/components/icon/IconArrowNext";
import BaseButton from "@/components/base/BaseButton";
import BaseTable from "@/components/base/BaseTable";
export default {
  components: {BaseTable, BaseButton, IconArrowNext, IconOrder, BaseNotice},
  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },
}
</script>


<style lang="scss" scoped>
.acc-biling {
  &__main {
    background: #E7F6FB;
    border-radius: 16px;
    padding: 59px 40px 64px;
    min-height: 550px;
    max-width: 1090px;
    width: 100%;
    margin: 0 auto;
    display: flex;
  }

  &__order {
    max-width: 420px;
    width: 100%;
    background: #FFFFFF;
    border-radius: 16px;
    padding: 76px 30px 60px;
    display: flex;
    flex-direction: column;
    align-items: center;

    p {
      font-weight: 500;
      font-size: 20px;
      line-height: 29px;
      text-align: center;
      color: #576280;
      margin: 25px 0 6px;
    }

    span {
      font-size: 14px;
      line-height: 20px;
      text-align: center;
      color: rgba(87, 98, 128, 0.6);
      margin-bottom: 18px;
    }

    a {
      color: #00B4DB;
    }
  }

  &__order-btn {
    margin-bottom: 16px;
    svg {
      margin-left: 10px;
    }
  }

  &__history {
    margin-left: 80px;
    width: 100%;
  }

  &__title {
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    text-transform: uppercase;
    color: #576280;
    opacity: 0.4;
    margin: 0;
  }

}
</style>
