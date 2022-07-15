<template>
  <div class="tabs">
    <ul class="tabs__header">
      <li
        v-for="title in tabTitles"
        :key="title"
        :class="[
          'tabs__title',
          { 'tabs__title--selected': selectedTitle === title },
        ]"
        @click="selectTitle(title)"
      >
        {{ title }}
      </li>
    </ul>
    <slot />
  </div>
</template>

<script>
export default {
  provide() {
    return {
      selectedTitle: this.selectedTitle
    }
  },

  data() {
    return {
      selectedTitle: ''
    }
  },

  computed: {
    tabTitles() {
      return this.$slots.default.map((tab) => tab?.componentOptions?.propsData.title).filter(title => title !== undefined)
    },
  },

  mounted() {
    console.log(this.$slots)
    this.selectedTitle = this.tabTitles[0]
  },

  methods: {
    selectTitle: (title) => {rr
      this.selectedTitle = ""
    }
  }
}
</script>

<style lang="scss" scoped>
.tabs {
  &__header {
    list-style: none;
    display: flex;
    border-radius: 16px;
    background: white;
    padding: 16px 20px;
    margin-bottom: 20px;
  }

  &__title {
    color: black;
    font-weight: bold;
    transition: color 0.5s;
    cursor: pointer;

    &:not(:last-child) {
      margin-right: 16px;
    }

    &:hover {
      color: red;
      opacity: 0.8;
    }
  }

  &__title--selected {
    color: red;
  }
}
</style>
