<template>
  <div class="container choice-block">
    <h2 class="base-title">{{ $t('title') }}</h2>
    <div class="choice-block__table-wrap">
      <choice-table class="choice-block__table" />
    </div>
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

  &__table-wrap {
    margin-bottom: 36px;
    width: 100%;

    @media(max-width: 1000px) {
      overflow-x: scroll;
    }
  }

  &__table {
    padding-bottom: 20px;
    @media(max-width: 1000px) {
      width: 960px;
    }
  }
}
</style>

