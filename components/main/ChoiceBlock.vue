<template>
  <div class="container choice-block">
    <h2 class="base-title">The best choice for you</h2>
    <choice-table class="choice-block__table" />
    <base-button>
      Get your VND key now
    </base-button>
  </div>
</template>

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

