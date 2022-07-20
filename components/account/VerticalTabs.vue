<template>
  <div class="tabs">
    <div class="tabs__header-wrap">
      <p class="tabs__header-title">
        {{ title }}
      </p>
      <ul class="tabs__header">
        <li
          v-for="(tab, index) in tabs"
          :key="tab.title"
          :class="{ tab__selected: index === selectedIndex }"
          @click="selectTab(index)"
        >
          <span>{{ tab.title }}</span>
        </li>
      </ul>
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ""
    }
  },

  data() {
    return {
      selectedIndex: 0,
      tabs: [],
    }
  },
  created() {
    this.tabs = this.$children
  },
  mounted() {
    this.selectTab(0)
  },
  methods: {
    selectTab(i) {
      this.selectedIndex = i

      // loop over all the tabs
      this.tabs.forEach((tab, index) => {
        tab.isActive = index === i
      })
    },
  },
}
</script>

<style lang="scss" scoped>
.tabs {
  display: flex;


  &__header-wrap {
    margin-right: 28px;
    max-width: 250px;
    width: 100%;
  }

  &__header-title {
    font-weight: 500;
    font-size: 16px;
    line-height: 23px;
    text-transform: uppercase;
    color: #576280;
    opacity: 0.4;
    margin: 0 0 7px;
  }

  &__header {
    display: flex;
    list-style: none;
    padding: 0;
    width: 100%;
    flex-direction: column;
    margin: 0;

    li {
      padding: 22px 0;
      font-size: 18px;
      line-height: 24px;
      color: #414141;
      cursor: pointer;
      width: 100%;
    }

    span {
      display: inline-flex;
      align-items: center;
    }

    svg {
      margin-right: 9px;
    }
  }
}

li.tab__selected {
  color: #00B4DB;
}
</style>
