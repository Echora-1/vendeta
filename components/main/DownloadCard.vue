<template>
  <div class="download-card">
    <div class="download-card__code">
      <img :src="require(`../../assets/img/${content.img}.png`)" width="154" height="151" alt="code">
    </div>
    <div>
      <p class="download-card__text">Select the type of device to download the application or use the qr-code.</p>
      <base-button>
        Download
      </base-button>
    </div>
  </div>
</template>
<script>
import BaseButton from "@/components/base/BaseButton";
export default {
  components: {BaseButton},
  props: {
    content: {
      type: Object,
      default: () => {
        return {
          img: 'code'
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.download-card {
  display: flex;
  align-items: center;

  &__code {
    min-width: 188px;
    height: 188px;
    background: #FFFFFF;
    border: 2px solid #F1F2F8;
    border-radius: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 39px;
  }

  &__text {
    font-size: 16px;
    line-height: 23px;
    color: #333333;
    opacity: 0.7;
    margin-bottom: 22px;
  }
}
</style>
