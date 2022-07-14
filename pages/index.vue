<template>
  <div>
    <div class="wrap-main-screen">
      <main-screen />
    </div>
    <div class="wrap-property-block">
      <property-block />
    </div>
    <div class="wrap-system-block">
      <system-block />
    </div>
    <div class="wrap-choice-block">
      <choice-block />
    </div>
  </div>
</template>

// 104.66 px на одну полоску
// 628px на 6
// 1256px на 12
// 32px между 2 блоками

<script>
import http from "http"
import MainScreen from "~/components/main/MainScreen";
import PropertyBlock from "~/components/main/PropertyBlock";
import SystemBlock from "~/components/main/SystemBlock";
import ChoiceBlock from "~/components/main/ChoiceBlock";
export default {
  components: {ChoiceBlock, SystemBlock, PropertyBlock, MainScreen},
  head() {
    return {
      title: 'Vendeta',
      link: [
        {
          rel: 'canonical',
          href: `http://localhost:3000${this.$route.path}`,
        },
      ],
    }
  },

  mounted() {
    setInterval(function () {
      http.get('http://app-vendeta.herokuapp.com/')
    }, 300000)
  }

}
</script>

<style lang="scss" scoped>
.wrap-main-screen,
.wrap-property-block,
.wrap-system-block,
.wrap-choice-block{
  z-index: 1;
  position: relative;
  overflow: visible;
}

.wrap-main-screen {
  position: relative;
  padding-bottom: 81px;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    width: 1445px;
    height: 749px;
    background-image: url("../assets/img/map.svg");
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;
    pointer-events: none;
  }

  &::after {
    content: "";
    position: absolute;
    right: -230.14px;
    top: 85px;
    width: 2452.13px;
    height: 1583.98px;
    mix-blend-mode: normal;
    filter: blur(150px);
    transform: rotate(-9.91deg);
    background: linear-gradient(89.98deg, rgba(152, 207, 225, 0) 5.81%, #98CFE1 98.35%);
    z-index: -2;
    pointer-events: none;
  }
}

.wrap-property-block {
  padding-bottom: 152px;
}

.wrap-system-block {
  padding-bottom: 125px;
}

.wrap-choice-block {
  padding-bottom: 180px;

  &::before {
    content: "";
    position: absolute;
    top: 175px;
    left: -200px;
    width: 2452.14px;
    height: 1583.98px;
    background: linear-gradient(89.98deg, rgba(152, 207, 225, 0) 5.81%, #98CFE1 98.35%);
    mix-blend-mode: normal;
    filter: blur(150px);
    transform: matrix(-0.99, -0.17, -0.17, 0.99, 0, 0);
    z-index: -1;
    pointer-events: none;
  }
}

</style>
