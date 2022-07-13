<template>
  <div>
    <div class="wrap-main-screen">
      <main-screen />
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
export default {
  components: {MainScreen},
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
.wrap-main-screen {
  position: relative;
  min-height: 200vh;
  z-index: 1;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    right: 78px;
    width: 1294px;
    height: 676px;
    background-image: url("../assets/img/map.svg");
    background-position: center;
    background-repeat: no-repeat;
    z-index: -1;
  }

  &::after {
    content: "";
    position: absolute;
    right: -230.14px;
    bottom: 304.1px;
    width: 2452.14px;
    height: 1583.98px;
    mix-blend-mode: normal;
    filter: blur(400px);
    transform: rotate(-9.91deg);
    background: linear-gradient(89.98deg, rgba(152, 207, 225, 0) 5.81%, #98CFE1 98.35%);
    z-index: -2;
  }
}
</style>
