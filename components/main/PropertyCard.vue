<template>
  <div class="property-card">
    <div class="property-card__img">
      <img :src="require(`../../assets/img/property/${content?.img}.svg`)" alt="icon">
    </div>
    <p class="property-card__title">{{ content?.title }}</p>
    <p class="property-card__text">{{ content?.text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      default: () => {
        return {

        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.property-card {
  display: flex;
  align-items: center;
  flex-direction: column;
  background: linear-gradient(180deg, #FFFFFF 0%, rgba(255, 255, 255, 0) 100%);
  border-radius: 24px;
  padding: 36px 34px 49px;

  &__img {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 88px;

  }

  &__title {
    font-weight: 500;
    font-size: 20px;
    line-height: 29px;
    color: #00B4DB;
    margin: 22px 0 18px;
  }

  &__text {
    margin: 0;
    font-size: 18px;
    line-height: 26px;
    text-align: center;
    color: #333333;
    opacity: 0.7;
    max-width: 320px;
  }
}
</style>
