<template>
  <div class="how-start">
    <p class="how-start__title">HOW TO START?</p>
    <div class="how-start__step">
      <p class="how-start__step-title"><span>Step 2/3:</span> Select your operating system</p>
      <div class="how-start__step-list">
        <div class="how-start__step-item">
          <icon-logo-android width="48" height="57" />
          <span>Android</span>
        </div>
        <div class="how-start__step-item">
          <icon-logo-i-o-s width="50" height="61" />
          <span>iOS</span>
        </div>
        <div class="how-start__step-item">
          <icon-logo-windows width="57" height="57" />
          <span>Windows</span>
        </div>
      </div>
    </div>
    <div class="how-start__actions">
      <base-button transparent class="how-start__instruction">
        Instruction .pdf
      </base-button>
      <base-button class="how-start__next">
        Next
        <icon-arrow-next />
      </base-button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.how-start {
  padding: 32px 34px 35px;
  background: #E7F6FB;
  width: 100%;
  border-radius: 16px;

  &__title {
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    color: #576280;
    opacity: 0.4;
    margin: 0 0 6px;
  }

  &__step-title {
    font-weight: 600;
    font-size: 28px;
    line-height: 40px;
    color: #576280;
    margin: 0 0 30px;

    span {
      color: rgba(87, 98, 128, 0.4);
    }
  }

  &__step-list {
    display: flex;
    margin-bottom: 29px;
  }

  &__step-item {
    width: calc((100% - 30px) / 3);
    background: #FFFFFF;
    border-radius: 16px;
    min-height: 267px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #576280;

    &:not(:last-child) {
      margin-right: 15px;
    }

    svg {
      margin-bottom: 23px;
    }

    span {
      font-weight: 500;
      font-size: 18px;
      line-height: 26px;
      color: #576280;
    }
  }

  &__actions {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__instruction {
    color: #576280;
  }

  &__next {
    display: flex;
    align-items: center;

    svg {
      margin-left: 10px;
    }
  }
}
</style>
<script>
import BaseButton from "@/components/base/BaseButton";
import IconLogoAndroid from "@/components/icon/IconLogoAndroid";
import IconLogoIOS from "@/components/icon/IconLogoIOS";
import IconLogoWindows from "@/components/icon/IconLogoWindows";
import IconArrowNext from "@/components/icon/IconArrowNext";
export default {
  components: {IconArrowNext, IconLogoWindows, IconLogoIOS, IconLogoAndroid, BaseButton}
}
</script>
