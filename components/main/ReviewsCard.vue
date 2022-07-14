<template>
  <div class="reviews-card">
    <p class="reviews-card__text">{{ content?.text }}</p>
    <div class="reviews-card__profile profile">
      <img class="profile__avatar" src="../../assets/img/avatar.svg" width="48" height="48" alt="avatar">
      <div>
        <p class="profile__name">{{ content?.name }}</p>
        <div class="profile__rating">
          <img v-for="(_, index) in content?.rating" :key="index" src="../../assets/img/star.svg" width="21" height="21" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      default: () => {

      }
    }
  }
}
</script>

<style lang="scss" scoped>
.profile {
  display: flex;

  &__name {
    font-weight: 600;
    font-size: 16px;
    line-height: 23px;
    color: #0A0A0A;
    opacity: 0.7;
    margin: 0 0 4px;
  }

  &__avatar {
    margin-right: 25px;
  }

  &__rating {
    display: flex;
  }
}

.reviews-card {
  display: flex;
  flex-direction: column;
  background: linear-gradient(180deg, #FFFFFF 0%, rgba(255, 255, 255, 0) 100%);
  border-radius: 24px;
  padding: 43px 33px 46px;

  &__text {
    font-size: 18px;
    line-height: 26px;
    color: #0A0A0A;
    opacity: 0.7;
    margin: 0 0 30px;
  }
}
</style>
