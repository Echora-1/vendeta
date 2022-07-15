<template>
  <div :class="['plan-card', { 'plan-card--save': content.save }]">
    <div v-show="content.save" class="plan-card__save">
      <span> {{ $t('save') }}{{ content.save }}% </span>
    </div>
    <p class="plan-card__duration">{{ content.duration }}</p>
    <div class="plan-card__icon">
      <img
        :src="require(`../../assets/img/${content.icon}.png`)"
        width="30"
        height="30"
        alt="icon"
      />
    </div>
    <p class="plan-card__price">${{ content.price }}<span>/mo</span></p>
    <base-button class="plan-card__btn" transparent>
      {{ $t('btn') }}
    </base-button>
    <p class="plan-card__sum">billed ${{ content.sum }} once</p>
  </div>
</template>

<i18n>
{
  "en": {
    "btn": "Select Plan",
    "save": "save "
  },
  "ch": {
    "btn": "Select Plan",
    "save": "save "
  },
  "tur": {
    "btn": "Select Plan",
    "save": "save "
  }
}
</i18n>

<script>
import BaseButton from '@/components/base/BaseButton'
export default {
  components: { BaseButton },

  props: {
    content: {
      type: Object,
      default: () => {
        return {
          icon: 'crystal',
        }
      },
    },
  },
}
</script>

<style lang="scss" scoped>
.plan-card {
  background: #ffffff;
  border-radius: 30px;
  padding: 43px 36px 33px;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  position: relative;

  &__save {
    text-transform: uppercase;
    position: absolute;
    background: #ff953f;
    transform: rotate(43deg);
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    text-align: center;
    color: #ffffff;
    min-width: 180px;
    min-height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    top: 32px;
    right: -46px;
  }

  p {
    text-align: center;
    margin-top: 0;
  }

  &__duration {
    font-size: 24px;
    line-height: 35px;
    margin-bottom: 36px;
  }

  &__icon {
    margin-bottom: 26px;
    width: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;

    img {
      width: 30px;
      height: 30px;
      object-fit: contain;
    }
  }

  &__price {
    font-weight: bold;
    font-size: 56px;
    line-height: 81px;
    color: #333333;
    margin-bottom: 31px;

    span {
      font-weight: bold;
      font-size: 28px;
      line-height: 40px;
      color: rgba(51, 51, 51, 0.6);
    }
  }

  &__btn {
    margin-bottom: 40px;
    min-width: 160px;
  }

  &__sum {
    font-weight: 600;
    font-size: 14px;
    line-height: 20px;
    color: #333333;
    opacity: 0.6;
  }
}
</style>
