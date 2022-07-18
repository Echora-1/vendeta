<template>
  <div class="overview-block">
    <div class="overview-block__header">
        <p class="overview-block__title">My Account</p>
        <div v-show="showNotice" class="overview-block__notice notice">
          <div class="notice__type">
            <span>Billing</span>
          </div>
          <p class="notice__text">key expired in 3 days</p>
          <button class="notice__close" @click="showNotice = false">
            <icon-close />
          </button>
        </div>
    </div>
    <div class="overview-block__main">
      <div class="overview-block__key-overview key-overview">
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
            <base-button>
              Billing
            </base-button>
          </div>
      </div>
      <how-to-start class="overview-block__how-to-start" />
    </div>
  </div>
</template>

<script>
import IconClose from "@/components/icon/IconClose";
import IconVendeta from "@/components/icon/IconVendeta";
import IconShow from "@/components/icon/IconShow";
import BaseButton from "@/components/base/BaseButton";
import HowToStart from "@/components/account/HowToStart";
export default {
  components: {HowToStart, BaseButton, IconShow, IconVendeta, IconClose},
  data() {
    return {
      showNotice: true,
      showKey: false,
    }
  },

  computed: {
    getKey() {
      return this.showKey ? 'X67Z HA31 KEC2  SAW5' : 'X67Z **** ****  SAW5'
    }
  }
}
</script>

<style lang="scss" scoped>
.overview-block {
  &__header {
    display: flex;
    align-items: center;
    min-height: 50px;
    margin-bottom: 35px;
  }

  &__title {
    font-weight: 500;
    font-size: 28px;
    line-height: 40px;
    color: #576280;
    margin: 0;
  }

  &__notice {
    margin-left: auto;
    max-width: 668px;
  }

  &__main {
    display: flex;
    align-items: flex-start;
  }

  &__key-overview {
    max-width: 370px;
  }

  &__how-to-start {
    max-width: 668px;
    margin-left: 66px;
  }
}

.key-overview {
  border-radius: 16px;
  overflow: hidden;
  width: 100%;

  &__wrap {
    padding: 35px 28px 28px 33px;
    background: linear-gradient(180deg, #99EDFF 0%, #00B4DB 100%);
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
      color: #FFFFFF;
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
      color: #FFFFFF;
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
    background: #E7F6FB;
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

.notice {
  width: 100%;
  display: flex;
  align-items: center;
  border: 1px solid #00B4DB;
  border-radius: 30px;
  min-height: 50px;
  padding: 4px 5px;

  &__type {
    background: #00B4DB;
    border-radius: 40px;
    font-weight: 500;
    font-size: 18px;
    line-height: 26px;
    color: #FFFFFF;
    min-height: 40px;
    padding: 7px 25px;
    margin-right: 18px;
  }

  &__text {
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    color: #576280;
    margin: 0;
  }

  &__close {
    cursor: pointer;
    border: none;
    width: 28px;
    height: 28px;
    margin-left: auto;
    margin-right: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: transparent;
    padding: 0;
  }
}
</style>
