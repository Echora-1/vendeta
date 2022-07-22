<template>
  <header>
    <div :class="['base-header', { 'base-header--menu-open': isShowMenu }]">
      <div class="base-header__inner-wrap">
        <nuxt-link :to="localePath('/')">
          <icon-logo class="base-header__logo" />
        </nuxt-link>
        <nav class="base-header__nav">
          <nuxt-link
            @click.native="closeMenu"
            :to="localePath(link.url)"
            class="base-header__link"
            v-for="(link, index) in $t('links')"
            :key="index"
          >
            {{ link.name }}</nuxt-link
          >
          <div class="base-header__actions">
            <span class="base-header__language">EN</span>
            <nuxt-link :to="localePath('/')">
              <base-button class="base-header__sign-up" transparent>
                Sign Up
              </base-button>
            </nuxt-link>
          </div>
        </nav>
        <menu-button
          class="base-header__menu-button"
          :active="isShowMenu"
          @click.native="toggleShowMenu"
        />
      </div>
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
  data() {
    return {
      isShowMenu: false,
    }
  },

  watch: {
    isShowMenu() {
      if (this.isShowMenu && window.innerWidth < 1001) {
        document.body.style.overflow = 'hidden'
      } else {
        document.body.style.overflow = 'visible'
      }
    },
  },

  mounted() {
    window.addEventListener('scroll', this.scrollHeader)
  },

  methods: {
    toggleShowMenu() {
      this.isShowMenu = !this.isShowMenu
    },

    closeMenu() {
      this.isShowMenu = false
    },

    scrollHeader() {
      const header = document.querySelector('.base-header')
      const headerWrap = document.querySelector('.base-header__wrap')
      if (window.scrollY >= 100) {
        header.classList.add('base-header--scroll')
        headerWrap.classList.add('base-header__wrap--scroll')
      } else {
        header.classList.remove('base-header--scroll')
        headerWrap.classList.remove('base-header__wrap--scroll')
      }
    },
  },
}
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  position: relative;
  z-index: 10;
}

.base-header {
  min-height: 45px;
  position: fixed;
  top: 0;
  width: 100%;

  &__inner-wrap {
    display: flex;
    align-items: center;
    max-width: 1280px;
    padding: 40px 20px 40px;
    margin: 0 auto;
  }

  &--scroll {
    background: linear-gradient(
      180deg,
      #c3e3ef 65%,
      rgba(255, 255, 255, 0) 100%
    );

    .base-header__inner-wrap {
      padding-top: 20px;
    }
  }

  &--menu-open {
    background: #c3e3ef;
    transition: all 1s;

    @media (max-width: 1000px) {
      .base-header__nav {
        opacity: 1;
        transform: translateX(0);
      }
    }
  }

  &__logo {
    width: 150px;
    height: 35px;
  }

  &__nav {
    display: flex;

    @media (max-width: 1000px) {
      position: absolute;
      left: 0;
      right: 0;
      bottom: calc(65px - 100vh);
      background: linear-gradient(
        180deg,
        #c3e3ef 55%,
        rgba(255, 255, 255, 0) 100%
      );
      padding: 15px 26px 20px;
      min-height: calc(100vh - 65px);
      opacity: 0;
      transform: translateX(200%);
      transition: transform 1s;
      flex-wrap: wrap;
      flex-direction: column;
      align-items: flex-start;
      justify-content: flex-start;
    }

    @media (min-width: 1001px) {
      margin-left: auto;
      align-items: center;
    }
  }

  &__link {
    font-size: 18px;
    line-height: 26px;
    opacity: 0.6;
    color: #000000;

    @media (min-width: 1001px) {
      &:not(:first-child) {
        margin-left: 73px;
      }
    }

    @media (max-width: 1000px) {
      font-size: 24px;
      line-height: 125%;

      &:not(:last-child) {
        margin-bottom: 32px;
      }
    }
  }

  &__actions {
    display: flex;
    align-items: center;

    @media (max-width: 1000px) {
      margin: 0 0 20px;
      order: -1;
      width: 100%;
      justify-content: space-between;
    }
  }

  &__language {
    @media (min-width: 1001px) {
      margin-left: 73px;
    }
  }

  &__sign-up {
    margin-left: 63px;
    min-height: 45px;
    font-size: 16px;
    line-height: 23px;
    min-width: 134px;
  }

  &__menu-button {
    margin-left: auto;
    @media (min-width: 1001px) {
      display: none;
    }
  }
}
</style>
