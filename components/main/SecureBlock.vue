<template>
  <div class="secure-block container">
    <h2 class="base-title">{{ $t('title') }}</h2>
    <p class="base-subtitle">{{ $t('subtitle') }}</p>
    <base-button>
      {{ $t('btn') }}
    </base-button>
  </div>
</template>

<i18n>
{
  "en": {
    "title": "Secure your digital life today",
    "subtitle": "100% money-back guarantee for your first 30 days.",
    "btn": "Get VND key"
  },
  "ch": {
    "title": "Secure your digital life today",
    "subtitle": "100% money-back guarantee for your first 30 days.",
    "btn": "Get VND key"
  },
  "tur": {
    "title": "Secure your digital life today",
    "subtitle": "100% money-back guarantee for your first 30 days.",
    "btn": "Get VND key"
  }
}
</i18n>

<script>
import BaseButton from "@/components/base/BaseButton";
export default {
  components: {BaseButton}
}
</script>

<style lang="scss" scoped>
.base-title {
  margin-bottom: 0;

  @media(max-width: 767px) {
    max-width: 300px;
    text-align: center;
  }
}

.base-subtitle {
  margin-bottom: 26px;

  @media(max-width: 767px) {
    max-width: 260px;
    text-align: center;
  }
}

.secure-block {
  display: flex;
  flex-direction: column;
  align-items: center;


}
</style>
