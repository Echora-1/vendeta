<template>
  <div class="wrap-sign-up">
    <div class="container sign-up">
      <wrap-form class="sign-up__form">
        <sign-up />
      </wrap-form>
    </div>
  </div>
</template>

<script>
import WrapForm from "~/components/WrapForm.vue";
import SignUp from "~/components/forms/SignUp.vue";
export default {
  components: {WrapForm, SignUp},
}
</script>

<style lang="scss" scoped>
.wrap-sign-up {
  z-index: 1;
  position: relative;


  &::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 1445px;
    height: 749px;
    background-image: url('../assets/img/map.svg');
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;
    pointer-events: none;
    background-size: contain;

    @media (max-width: 767px) {
      width: 1128px;
      height: 591px;
      left: -137px;
      top: -5px;
    }
  }

  &::after {
    content: '';
    position: absolute;
    right: -230.14px;
    top: 85px;
    width: 2452.13px;
    height: 1583.98px;
    mix-blend-mode: normal;
    filter: blur(150px);
    transform: rotate(-9.91deg);
    background: linear-gradient(
        89.98deg,
        rgba(152, 207, 225, 0) 5.81%,
        #98cfe1 98.35%
    );
    z-index: -2;
    pointer-events: none;
  }
}

.sign-up {
  display: flex;
  min-height: 100vh;
  padding-top: 220px;
  position: relative;

  &__form {
    position: absolute;
    top: calc(50% - 220px);
    left: 50%;
    transform: translate(-50%);
  }
}
</style>
