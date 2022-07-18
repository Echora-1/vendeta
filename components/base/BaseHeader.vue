<template>
  <header class="container">
    <div class="base-header">
      <nuxt-link :to="localePath('/')">
        <icon-logo class="base-header__logo" />
      </nuxt-link>
      <ul class="base-header__nav">
        <li
          class="base-header__link"
          v-for="(link, index) in $t('links')"
          :key="index"
        >
          <nuxt-link :to="localePath(link.url)"> {{ link.name }}</nuxt-link>
        </li>
      </ul>
      <span class="base-header__language">EN</span>
      <nuxt-link :to="localePath('/')">
        <base-button class="base-header__sign-up" transparent>
          Sign Up
        </base-button>
      </nuxt-link>
    </div>
  </header>
</template>

<i18n>
{
  "en": {
    "links": [ { "name": "Plans", "url": "/plans" }, { "name": "Tokenomics", "url": "/account" }, { "name": "Launch Pool", "url": "/" }]
  },
  "ch": {
    "links": [ { "name": "Plans", "url": "/plans" }, { "name": "Tokenomics", "url": "/account" }, { "name": "Launch Pool", "url": "/" }]
  },
  "tur": {
    "links": [ { "name": "Plans", "url": "/plans" }, { "name": "Tokenomics", "url": "/account" }, { "name": "Launch Pool", "url": "/" }]
  }
}
</i18n>

<script>
import IconLogo from '~/components/icon/IconLogo'
import BaseButton from '~/components/base/BaseButton'
export default {
  components: { BaseButton, IconLogo },
}
</script>

<style lang="scss" scoped>
.container {
  position: relative;
  z-index: 10;
}

.base-header {
  display: flex;
  align-items: center;
  min-height: 45px;
  position: fixed;
  top: 40px;
  width: 100%;
  max-width: 1240px;

  &__logo {
    width: 150px;
    height: 35px;
  }

  &__nav {
    margin: 0 0 0 auto;
    list-style: none;
    padding-left: 0;
    display: flex;
  }

  &__link {
    font-size: 18px;
    line-height: 26px;
    opacity: 0.6;
    color: #000000;

    &:not(:first-child) {
      margin-left: 73px;
    }
  }

  &__language {
    margin-left: 73px;
  }

  &__sign-up {
    margin-left: 63px;
    min-height: 45px;
    font-size: 16px;
    line-height: 23px;
    min-width: 134px;
  }
}
</style>
