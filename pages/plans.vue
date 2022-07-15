<template>
  <div>
    <div class="wrap-plan-block">
      <plan-block />
    </div>
    <div class="wrap-faq-block">
     <faq-block />
    </div>
  </div>
</template>

<script>

import PlanBlock from "@/components/plans/PlanBlock";
import FaqBlock from "@/components/plans/FaqBlock";
export default {
  components: {PlanBlock, FaqBlock},
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
}
</script>

<style lang="scss" scoped>
.wrap-plan-block,
.wrap-faq-block {
  z-index: 1;
  position: relative;
  overflow: visible;
}

.wrap-plan-block {
  padding-top: 175px;
  padding-bottom: 46px;
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

.wrap-faq-block {
  padding-bottom: 122px;
}
</style>
