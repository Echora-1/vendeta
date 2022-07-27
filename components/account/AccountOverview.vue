<template>
  <div class="acc-overview">
    <div class="account-header">
      <p class="account-header__title">My Account</p>
      <base-notice
        v-show="showNotice"
        class="account-header__notice"
        @close="showNotice = false"
      />
    </div>
    <div class="acc-overview__main">
      <div class="acc-overview__key-overview key-overview">
        <div class="key-overview__wrap">
          <div class="key-overview__title">
            <icon-vendeta />
            <p>Your VPN key</p>
          </div>
          <div class="key-overview__key">
            <p>{{ getKey }}</p>
            <button class="key-overview__key-show" @click="showKey = !showKey">
              <icon-show />
            </button>
          </div>
        </div>
        <div class="key-overview__expires">
          <div class="key-overview__expires-text">
            <span>expires in:</span>
            <p>3 Days</p>
          </div>
          <base-button> Billing </base-button>
        </div>
      </div>
      <how-to-start class="acc-overview__how-to-start" />
    </div>
  </div>
</template>

<script>
import IconVendeta from '@/components/icon/IconVendeta'
import IconShow from '@/components/icon/IconShow'
import BaseButton from '@/components/base/BaseButton'
import HowToStart from '@/components/account/HowToStart'
import BaseNotice from '@/components/base/BaseNotice'
export default {
  components: { BaseNotice, HowToStart, BaseButton, IconShow, IconVendeta },
  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },

  computed: {
    getKey() {
      return this.showKey ? 'X67Z HA31 KEC2  SAW5' : 'X67Z **** ****  SAW5'
    },
  },
}
</script>

<style lang="scss" scoped>
.acc-overview {
  &__main {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
  }

  &__key-overview {
    max-width: 370px;
  }

  &__how-to-start {
    max-width: 668px;
    margin-left: 10px;
  }
}

.key-overview {
  border-radius: 16px;
  overflow: hidden;
  width: 100%;

  &__wrap {
    padding: 35px 28px 28px 33px;
    background: linear-gradient(180deg, #99edff 0%, #00b4db 100%);
  }

  &__title {
    display: flex;
    align-items: center;
    margin-bottom: 16px;

    svg {
      width: 48px;
      height: 54px;
      margin-right: 20px;
    }

    p {
      font-weight: 500;
      font-size: 18px;
      line-height: 26px;
      color: #ffffff;
      margin: 0;
    }
  }

  &__key {
    display: flex;
    align-items: center;
    justify-content: space-between;

    p {
      font-weight: 500;
      font-size: 24px;
      line-height: 35px;
      color: #ffffff;
      margin: 0;
    }

    svg {
      width: 20px;
      height: 15px;
    }
  }

  &__key-show {
    cursor: pointer;
    border: none;
    width: 25px;
    height: 25px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: transparent;
    padding: 0;
  }

  &__expires {
    padding: 31px 28px 28px 33px;
    display: flex;
    background: #e7f6fb;
    align-items: center;
    justify-content: space-between;
  }

  &__expires-text {
    span {
      font-weight: 500;
      font-size: 16px;
      line-height: 23px;
      color: #576280;
      opacity: 0.4;
      text-transform: uppercase;
    }

    p {
      font-weight: 600;
      font-size: 28px;
      line-height: 40px;
      color: #576280;
      margin: 0;
    }
  }
}
</style>
