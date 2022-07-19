<template>
  <div class="acc-download-card">
    <div class="acc-download-card__icon-wrap">
      <component :is="content.icon" :width="content.iconWidth"  :height="content.iconHeight"></component>
    </div>
    <p class="acc-download-card__platform">{{ content.platform }}</p>
    <p class="acc-download-card__ver">{{ content.ver }}</p>
    <span class="acc-download-card__update">{{ content.update }}</span>
    <button class="acc-download-card__btn">
      {{ $t('download')}}
    </button>
  </div>
</template>

<i18n>
{
  "en": {
    "download": "Download"
  },
  "ch": {
    "download": "Download"
  },
  "tur": {
    "download": "Download"
  }
}
</i18n>

<script>
import IconLogoIOS from "@/components/icon/IconLogoIOS";
import IconLogoWindows from "@/components/icon/IconLogoWindows";
import IconLogoAndroid from "@/components/icon/IconLogoAndroid";
import IconLogoMacos from "@/components/icon/IconLogoMacos";
export  default {
  components: {IconLogoMacos, IconLogoAndroid, IconLogoWindows, IconLogoIOS},
  props: {
    content: {
      type: Object,
      default: () => {
        return {
          icon: "IconLogoWindows",
          iconWidth: 57,
          iconHeight: 57
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.acc-download-card {
  min-height: 320px;
  background: #FFFFFF;
  border-radius: 16px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 42px 20px 41px;
  color: #576280;

  &__icon-wrap {
    height: 61px;
  }

  &__platform {
    font-weight: 500;
    font-size: 18px;
    line-height: 26px;
    color: #576280;
    margin: 22px 0 32px;
  }

  &__ver,
  &__update {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: #576280;
    margin: 0;
  }

  &__update {
    color: rgba(87, 98, 128, 0.6);
    margin-bottom: 32px;
  }

  &__btn {
    border: none;
    color: #00B4DB;
    background: transparent;
    cursor: pointer;
  }
}
</style>
