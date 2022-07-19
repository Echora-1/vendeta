<template>
  <div class="acc-setting-card">
    <div class="acc-setting-card__icon-wrap">
      <component :is="content.icon" :width="content.iconWidth"  :height="content.iconHeight"></component>
    </div>
    <p class="acc-setting-card__name">{{ content.name }}</p>
    <p class="acc-setting-card__title">{{ content.title }}</p>
    <p class="acc-setting-card__text">{{ content.text }}</p>
    <button>
      {{ content.btn }}
    </button>
  </div>
</template>

<script>
import IconTwofa from "@/components/icon/IconTwofa";
import IconDeletion from "@/components/icon/IconDeletion";
import IconAccount from "@/components/icon/IconAccount";
export default {
  components: {IconAccount, IconDeletion, IconTwofa},
  props: {
    content: {
      type: Object,
      default: () => {
        return {
          icon: "IconAccount",
          iconWidth: "60",
          iconHeight: "59"
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.acc-setting-card {
  background: #FFFFFF;
  border-radius: 16px;
  padding: 47px 20px 36px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 320px;

  &__icon-wrap {
    height: 61px;
    margin-bottom: 20px;
  }

  &__name {
    font-weight: 500;
    font-size: 18px;
    line-height: 26px;
    text-align: center;
    color: #576280;
    margin: 0 0 27px;
  }

  &__title {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: #576280;
    margin: 0 0 7px;
  }

  &__text {
    font-size: 16px;
    line-height: 23px;
    text-align: center;
    color: #576280;
    margin: 0 0 32px;
  }

  button {
    font-size: 16px;
    line-height: 23px;
    text-align: center;
    color: #00B4DB;
    border: none;
    background: transparent;
    margin-top: auto;
    cursor: pointer;
  }
}
</style>
