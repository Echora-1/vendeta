<template>
  <button :class="['base-button', {'base-button--transparent': transparent }]">
    <slot> </slot>
  </button>
</template>

<script>
export default {
  props: {
    transparent: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style lang="scss" scoped>
.base-button {
  color: #FFFFFF;
  font-weight: 500;
  font-size: 18px;
  line-height: 26px;
  padding: 9px 26px;
  border: 2px solid #00b4db;
  border-radius: 30px;
  background: #00b4db;
  cursor: pointer;
  min-height: 55px;
  text-align: center;

  &--transparent {
    color: #00b4db;
    background: transparent;
  }
}
</style>
