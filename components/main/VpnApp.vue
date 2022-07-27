<template>
  <div :class="['vpn-app', { 'vpn-app--animatiom': animation }]">
    <div class="vpn-app__stat">
      <p class="vpn-app__stat-title">Statistics</p>
      <icon-stat class="vpn-app__stat-icon" />
      <div class="vpn-app__stat-speed">
        <div class="vpn-app__stat-item">
          <p>956 B/s</p>
          <span>max download speed</span>
        </div>
        <div class="vpn-app__stat-item">
          <p>286 B/s</p>
          <span>max upload speed</span>
        </div>
      </div>
    </div>
    <div class="vpn-app__app">
      <p class="vpn-app__status">VPN Disabled</p>
      <p class="vpn-app__work-timer">00 : 00 : 00</p>
      <div class="vpn-app__toggle-wrap">
        <div class="vpn-app__toggle">
          <icon-toggle />
        </div>
      </div>
      <div class="vpn-app__speed">
        <div class="vpn-app__speed-item">
          <p>682 B/s</p>
          <span>download</span>
        </div>
        <div class="vpn-app__speed-item">
          <p>208 B/s</p>
          <span>upload</span>
        </div>
      </div>
      <div class="vpn-app__region">
        <span>230:521:320:24</span>
        <p>North America - Canada</p>
      </div>
      <div class="vpn-app__buttons">
        <div class="vpn-app__btn">
          <icon-setting />
        </div>
        <div class="vpn-app__btn vpn-app__btn--active">
          <icon-vendeta />
        </div>
        <div class="vpn-app__btn">
          <icon-graph />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import IconToggle from '@/components/icon/IconToggle'
import IconSetting from '@/components/icon/IconSetting'
import IconVendeta from '@/components/icon/IconVendeta'
import IconGraph from '@/components/icon/IconGraph'
import IconStat from '@/components/icon/IconStat'
export default {
  components: { IconStat, IconGraph, IconVendeta, IconSetting, IconToggle },

  data() {
    return {
      animation: false,
    }
  },

  mounted() {
    document.addEventListener('DOMContentLoaded',  () => {
      this.animation = true
    })
  },
}
</script>

<style lang="scss" scoped>
.vpn-app {
  position: relative;

  &--animatiom {
    .vpn-app__toggle-wrap {
      background: #00b4db;
    }

    .vpn-app__toggle {
      transform: translate(48px, -50%);
      color: #00b4db;
    }
  }

  &__app {
    width: 320px;
    min-height: 693px;
    background: linear-gradient(
      180deg,
      #ffffff 0%,
      rgba(255, 255, 255, 0) 100%
    );
    border-radius: 36px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 139px;
    padding: 20px;
  }

  &__status {
    font-size: 20px;
    line-height: 29px;
    text-align: center;
    color: #989898;
    margin-top: 49px;
    margin-bottom: 0;
  }

  &__work-timer {
    font-size: 20px;
    line-height: 29px;
    text-align: center;
    color: #333333;
    display: inline-block;
    padding-left: 13px;
    overflow: visible;
    position: relative;
    margin-top: 8px;
    margin-bottom: 75px;

    &:before {
      content: '';
      position: absolute;
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: #db0000;
      left: -2px;
      top: 50%;
      transform: translateY(-50%);
    }
  }

  &__toggle-wrap {
    background: #a1c7d2;
    box-shadow: inset 0 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 100px;
    width: 124px;
    height: 48px;
    position: relative;
    margin-bottom: 79px;
    transition: all 0.3s;
  }

  &__toggle {
    position: absolute;
    background: #ffffff;
    box-shadow: 0 4px 24px rgba(0, 0, 0, 0.1);
    width: 76px;
    height: 76px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    color: #a1c7d2;
    top: 50%;
    left: 0;
    transform: translate(0, -50%);
    transition: all 0.3s;
  }

  &__speed {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 254px;
    margin-bottom: 44px;
  }

  &__speed-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 16px;

    p {
      font-size: 24px;
      line-height: 35px;
      text-align: center;
      color: #333333;
      margin: 0;
    }

    span {
      font-size: 12px;
      line-height: 17px;
      text-align: center;
      text-transform: uppercase;
      color: rgba(51, 51, 51, 0.6);
    }
  }

  &__region {
    background: rgba(155, 154, 186, 0.1);
    box-shadow: inset 0 4px 4px rgba(60, 55, 199, 0.05);
    border-radius: 12px;
    min-height: 82px;
    width: 254px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 31px;

    span {
      font-size: 14px;
      line-height: 20px;
      text-align: center;
      color: rgba(51, 51, 51, 0.6);
    }

    p {
      font-size: 20px;
      line-height: 29px;
      text-align: center;
      color: #333333;
      margin: 0;
    }
  }

  &__buttons {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 254px;
  }

  &__btn {
    width: 74px;
    height: 74px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;

    &--active {
      background: #ffffff;
      box-shadow: inset 0px 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 12px;
    }
  }

  &__stat {
    position: absolute;
    background: #ffffff;
    border-radius: 36px;
    width: 308px;
    min-height: 256px;
    display: flex;
    flex-direction: column;
    align-items: center;
    top: 305px;
    left: -4px;
    filter: drop-shadow(0px 8px 24px rgba(0, 0, 0, 0.08));
  }

  &__stat-title {
    font-size: 24px;
    line-height: 35px;
    text-align: center;
    color: #333333;
    margin-top: 23px;
  }

  &__stat-icon {
    margin-bottom: 33px;
  }

  &__stat-speed {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 254px;
  }

  &__stat-item {
    padding: 0 3px;

    &:last-child {
      margin-right: 11px;
    }

    p {
      font-size: 20px;
      line-height: 23px;
      text-align: center;
      color: #333333;
      margin: 0;
    }

    span {
      font-size: 10px;
      line-height: 14px;
      text-align: center;
      text-transform: uppercase;
      color: rgba(51, 51, 51, 0.6);
    }
  }
}
</style>
