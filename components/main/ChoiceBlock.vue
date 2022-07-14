<template>
  <div class="container choice-block">
    <h2 class="base-title">{{ $t('title') }}</h2>
    <choice-table class="choice-block__table" />
    <base-button>
      {{ $t('button') }}
    </base-button>
  </div>
</template>

<i18n>
{
  "en": {
    "title": "The best choice for you",
    "button": "Get your VND key now"
  },
  "ch": {
    "title": "The best choice for you",
    "button": "Get your VND key now"
  },
  "tur": {
    "title": "The best choice for you",
    "button": "Get your VND key now"
  }
}
</i18n>

<script>
import ChoiceTable from "~/components/main/ChoiceTable";
import BaseButton from "~/components/base/BaseButton";
export default {
  components: {BaseButton, ChoiceTable}
}
</script>

<style lang="scss" scoped>
.base-title {
  margin-bottom: 78px;
}

.choice-block {
  display: flex;
  flex-direction: column;
  align-items: center;

  &__table {
    margin-bottom: 56px;
  }
}
</style>

