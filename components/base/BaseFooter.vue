<template>
  <footer class="base-footer container">
    <div class="base-footer__main">
      <div class="base-footer__nav">
        <ul>
          <li
            class="base-footer__link"
            v-for="(link, index) in $t('links')"
            :key="index"
          >
            <nuxt-link :to="localePath(link.url)">{{link.name}}</nuxt-link>
          </li>
        </ul>
      </div>
      <div class="base-footer__social">
        <ul>
          <li class="base-footer__link">
            <a href="/" target="_blank"
              ><span class="base-footer__social-icon"><icon-telegram /></span>
              <span>Telegram</span></a
            >
          </li>
          <li class="base-footer__link">
            <a href="/" target="_blank"
              ><span class="base-footer__social-icon"><icon-facebook /></span>
              <span>Facebook</span></a
            >
          </li>
          <li class="base-footer__link">
            <a href="/" target="_blank"
              ><span class="base-footer__social-icon"><icon-twitter /></span>
              <span>Twitter</span></a
            >
          </li>
        </ul>
      </div>
    </div>
    <div class="base-footer__copyright">
      <p>{{ $t('copyright')}}</p>
    </div>
  </footer>
</template>

<i18n>
{
  "en": {
    "links": [
      {
        "name": "What is a VPN",
        "url": "/"
      },
      {
        "name": "VPN free trial",
        "url": "/"
      },
      {
        "name": "VPN download",
        "url": "/"
      },
      {
        "name": "Help center",
        "url": "/"
      },
      {
        "name": "VPN tutorials",
        "url": "/"
      },
      {
        "name": "Contact us",
        "url": "/"
      },
      {
        "name": "Privacy policy",
        "url": "/"
      },
      {
        "name": "Terms & conditions",
        "url": "/"
      }
    ],
    "copyright": "Copyright © 2022, All right reserved."
  },
  "ch": {
    "links": [
      {
        "name": "What is a VPN",
        "url": "/"
      },
      {
        "name": "VPN free trial",
        "url": "/"
      },
      {
        "name": "VPN download",
        "url": "/"
      },
      {
        "name": "Help center",
        "url": "/"
      },
      {
        "name": "VPN tutorials",
        "url": "/"
      },
      {
        "name": "Contact us",
        "url": "/"
      },
      {
        "name": "Privacy policy",
        "url": "/"
      },
      {
        "name": "Terms & conditions",
        "url": "/"
      }
    ],
    "copyright": "Copyright © 2022, All right reserved."
  },
  "tur": {
    "links": [
      {
        "name": "What is a VPN",
        "url": "/"
      },
      {
        "name": "VPN free trial",
        "url": "/"
      },
      {
        "name": "VPN download",
        "url": "/"
      },
      {
        "name": "Help center",
        "url": "/"
      },
      {
        "name": "VPN tutorials",
        "url": "/"
      },
      {
        "name": "Contact us",
        "url": "/"
      },
      {
        "name": "Privacy policy",
        "url": "/"
      },
      {
        "name": "Terms & conditions",
        "url": "/"
      }
    ],
    "copyright": "Copyright © 2022, All right reserved."
  }
}
</i18n>

<script>
import IconTwitter from '@/components/icon/IconTwitter'
import IconFacebook from '@/components/icon/IconFacebook'
import IconTelegram from '@/components/icon/IconTelegram'
export default {
  components: { IconTelegram, IconFacebook, IconTwitter },
}
</script>

<style lang="scss" scoped>
.base-footer {
  position: relative;
  z-index: 1;

  &__main {
    display: flex;

    @media(max-width: 767px) {
      flex-direction: column;
      align-items: center;
    }
  }

  &__nav {
    max-width: 920px;
    width: 100%;

    @media(min-width: 768px) {
      padding-bottom: 55px;
    }

    ul {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0;

      @media (min-width: 768px) {
        display: block;
        -webkit-columns: 3;
        -moz-columns: 3;
        -moz-column-count: 3;
        column-count: 3;
      }
    }

    li {
      @media (max-width: 767px) {
        margin-bottom: 40px;

        &:nth-child(3n) {
          margin-bottom: 60px;
        }
      }

      @media (min-width: 768px) {
        margin-bottom: 30px;
      }
    }
  }

  &__link {
    font-size: 16px;
    line-height: 125%;
    color: #33333399;

    a {
      font-size: 16px;
      line-height: 125%;
      color: #33333399;
    }
  }

  &__social {
    @media(min-width: 768px) {
      padding-left: 30px;
    }

    @media(max-width: 767px) {
      padding-bottom: 35px;
    }

    ul {
      margin: 0;

      @media(max-width: 767px) {
        display: flex;
        flex-direction: column;
        align-items: center;
      }

    }

    li:not(:last-child) {
      margin-bottom: 30px;
    }

    a {
      display: inline-flex;
      align-items: center;
    }
  }

  &__social-icon {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 20px;
    height: 20px;
    margin-right: 6px;

    @media(max-width: 767px) {
      margin-bottom: 1px;
    }
  }

  &__copyright {
    display: flex;
    justify-content: center;
    padding-bottom: 22px;

    @media(max-width: 767px) {
      padding-bottom: 60px;
    }

    p {
      font-size: 14px;
      line-height: 20px;
      text-align: center;
      color: #333333;
      opacity: 0.4;
    }
  }
}
</style>
