<template>
  <div>
    <div class="wrap-account-block">
      <account-block />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrap-account-block {
  padding-top: 138px;
  padding-bottom: 69px;
  position: relative;
  z-index: 1;

  &::after {
    content: "";
    top: 70px;
    right: -230.14px;
    position: absolute;
    width: 2452.14px;
    height: 1583.98px;
    background: linear-gradient(89.98deg, rgba(152, 207, 225, 0) 5.81%, #98CFE1 98.35%);
    mix-blend-mode: normal;
    filter: blur(150px);
    transform: rotate(-9.91deg);
    z-index: -1;
    pointer-events: none;
  }
}
</style>
<script>
import AccountBlock from "@/components/account/AccountBlock";
export default {
  components: {AccountBlock}
}
</script>
