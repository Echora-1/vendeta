<template>
  <div class="overview-block__notice notice">
    <div class="notice__type">
      <span>Billing</span>
    </div>
    <p class="notice__text">key expired in 3 days</p>
    <button class="notice__close" @click="close">
      <icon-close />
    </button>
  </div>
</template>

<script>
import IconClose from "@/components/icon/IconClose";
export default {
  components: {IconClose},

  methods: {
    close() {
      this.$emit('close')
    }
  }
}
</script>

<style lang="scss" scoped>
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
